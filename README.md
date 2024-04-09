# Senana-3-Coursera
// Obtener la configuración regional del dispositivo
Locale locale = Locale.getDefault();

// Obtener el identificador del idioma
String language = locale.getLanguage();

// Cargar el archivo XML de strings para el idioma seleccionado
Resources resources = getResources();
int resId = resources.getIdentifier("strings_" + language, "xml", getPackageName());
XmlResourceParser parser = resources.getXml(resId);

// Leer las cadenas de texto del archivo XML
while (parser.next() != XmlResourceParser.END_DOCUMENT) {
  if (parser.getEventType() == XmlResourceParser.START_ELEMENT) {
    String name = parser.getName();
    String value = parser.getAttributeValue(null, "value");
    // ...
  }
}
