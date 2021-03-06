# xgin

## Dependencies

+ github.com/Aoi-hosizora/ahlib
+ github.com/gin-gonic/gin
+ github.com/sirupsen/logrus

## Documents

### Types

+ `type DumpRequestOption func`
+ `type AppRouter struct`

### Variables

+ `var PrintAppRouterRegisterFunc func(index, count int, method, relativePath, handlerFuncname string, handlersCount int, layerFakePath string)`

### Constants

+ None

### Functions

+ `func WithRetainHeaders(headers ...string) DumpRequestOption`
+ `func WithIgnoreHeaders(headers ...string) DumpRequestOption`
+ `func WithSecretHeaders(headers ...string) DumpRequestOption`
+ `func WithSecretReplace(secret string) DumpRequestOption`
+ `func DumpRequest(c *gin.Context, options ...DumpRequestOption) []string`
+ `func PprofWrap(router *gin.Engine)`
+ `func GetValidatorEngine() (*validator.Validate, error)`
+ `func GetValidatorTranslator(locTranslator locales.Translator, registerFn xvalidator.TranslationRegisterHandler) (ut.Translator, error)`
+ `func AddBinding(tag string, fn validator.Func) error`
+ `func AddTranslator(translator ut.Translator, tag, message string, override bool) error`
+ `func EnableRegexpBinding() error`
+ `func EnableRegexpBindingTranslator(translator ut.Translator) error`
+ `func EnableRFC3339DateBinding() error`
+ `func EnableRFC3339DateBindingTranslator(translator ut.Translator) error`
+ `func EnableRFC3339DateTimeBinding() error`
+ `func EnableRFC3339DateTimeBindingTranslator(translator ut.Translator) error`
+ `func WithExtraText(text string) logop.LoggerOption`
+ `func WithExtraFields(fields map[string]interface{}) logop.LoggerOption`
+ `func WithExtraFieldsV(fields ...interface{}) logop.LoggerOption`
+ `func LogToLogrus(logger *logrus.Logger, c *gin.Context, start, end time.Time, options ...logop.LoggerOption)`
+ `func LogToLogger(logger logrus.StdLogger, c *gin.Context, start, end time.Time, options ...logop.LoggerOption)`
+ `func NewAppRouter(engine *gin.Engine, router gin.IRouter) *AppRouter`

### Methods

+ `func (a *AppRouter) GET(relativePath string, handlers ...gin.HandlerFunc)`
+ `func (a *AppRouter) POST(relativePath string, handlers ...gin.HandlerFunc)`
+ `func (a *AppRouter) DELETE(relativePath string, handlers ...gin.HandlerFunc)`
+ `func (a *AppRouter) PATCH(relativePath string, handlers ...gin.HandlerFunc)`
+ `func (a *AppRouter) PUT(relativePath string, handlers ...gin.HandlerFunc)`
+ `func (a *AppRouter) OPTIONS(relativePath string, handlers ...gin.HandlerFunc)`
+ `func (a *AppRouter) HEAD(relativePath string, handlers ...gin.HandlerFunc)`
+ `func (a *AppRouter) Any(relativePath string, handlers ...gin.HandlerFunc)`
+ `func (a *AppRouter) Register()`
