---
title: Acerca del modelo de objetos de texto
description: En este tema se proporciona información general de alto nivel de TOM.
ms.assetid: e304ec18-ec2e-4ea7-91c6-6f6ab63b72ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b934aab1cbd3dca932b58e4aa99498843cb8cc97
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061407"
---
# <a name="about-text-object-model"></a>Acerca del modelo de objetos de texto

El Modelo de objetos de texto (TOM) define un conjunto de interfaces de manipulación de texto que son compatibles en distintos grados con varias soluciones de texto de Microsoft, incluido el control de edición enriquecido. En este tema se proporciona información general de alto nivel de TOM. Describe los temas siguientes.

-   [Objetos TOM versión 2](#tom-version-2-objects)
-   [Convenciones de interfaz TOM](#tom-interface-conventions)
-   [El tipo tomBool](#the-tombool-type)
-   [Compilación matemática y compilación](#math-buildup-and-build-down)
-   [TOM RTF](#tom-rtf)
-   [Buscar texto enriquecido](#finding-rich-text)
-   [Accesibilidad de TOM](#tom-accessibility)
    -   [Interfaz de la tabla de objetos en ejecución](#interface-from-running-object-table)
    -   [Interfaz de mensajes de ventana](#interface-from-window-messages)
    -   [Métodos orientados a la accesibilidad](#accessibility-oriented-methods)
-   [Juegos de coincidencias de caracteres](#character-match-sets)

## <a name="tom-version-2-objects"></a>Objetos TOM versión 2

TOM versión 2 (TOM 2) extiende el modelo de objetos de texto original; las nuevas interfaces se derivan de las antiguas. La API TOM actualizada incluye compatibilidad con nuevas propiedades de formato de caracteres y párrafos, un modelo de tabla, selección múltiple y compatibilidad con objetos en línea para matemáticas y ruby.

El objeto TOM 2 de nivel superior se define mediante la interfaz [**ITextDocument2,**](/windows/desktop/api/Tom/nn-tom-itextdocument2) que tiene métodos para crear y recuperar objetos inferiores en la jerarquía de objetos. Para un procesamiento sencillo de texto sin formato, puede obtener un objeto [**ITextRange2**](/windows/desktop/api/Tom/nn-tom-itextrange2) de un objeto **ITextDocument2** y hacer la mayoría de las cosas con eso. Si necesita agregar formato de texto enriquecido, puede obtener objetos [**ITextFont2**](/windows/desktop/api/Tom/nn-tom-itextfont2) e [**ITextPara2**](/windows/desktop/api/Tom/nn-tom-itextpara2) de un **objeto ITextRange2.** **ITextFont2 proporciona** el equivalente de programación del cuadro de diálogo Microsoft Word format-font y **ITextPara2** proporciona el equivalente del cuadro de diálogo formato-párrafo de Word.

Además de estos tres objetos de nivel inferior, TOM 2 tiene un objeto de selección ([**ITextSelection2**](/windows/win32/api/tom/nn-tom-itextselection2)), que es un objeto [**ITextRange2**](/windows/desktop/api/Tom/nn-tom-itextrange2) con resaltado de selección y algunos métodos orientados a la interfaz de usuario.

Los objetos de rango y selección incluyen métodos orientados a pantalla que permiten a los programas examinar texto en pantalla o texto que se podría desplazar a la pantalla. Estas funcionalidades ayudan a que el texto sea accesible para personas con discapacidades visuales, por ejemplo.

Cada interfaz que tiene el sufijo 2 hereda de la interfaz correspondiente sin el sufijo 2. Por ejemplo, [**ITextDocument2**](/windows/desktop/api/Tom/nn-tom-itextdocument2) hereda de [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument).

Los objetos TOM 2 tienen la siguiente jerarquía.

``` syntax
ITextDocument2         Top-level editing object
    ITextRange2        Primary text interface: a range of text
        ITextFont2     Character-attribute interface
        ITextPara2     Paragraph-attribute interface
        ITextRow       Table interface
    ITextSelection2    Screen highlighted text range
        ITextRange2    Selection inherits all range methods
    ITextDisplays      Displays collection (not yet defined)
    ITextStrings       Rich-text strings collection
    ITextStoryRanges2  Enumerator for stories in document
```

Un [**objeto ITextDocument2**](/windows/desktop/api/Tom/nn-tom-itextdocument2) describe uno o varios intervalos contiguos de texto *denominados casos.* Los casos representan varias partes de un documento, como el texto principal del documento, los encabezados y pies de página, las notas al pie, las anotaciones y los blocs de notas de texto enriquecido. Se usa una historia de bloc de notas cuando se traduce entre expresiones matemáticas con formato lineal y un formulario integrado. También se usa un caso de panel de scratch al guardar el contenido de un intervalo que es el origen de copia actual cuando el contenido está a punto de cambiarse.

Un [**objeto ITextRange2**](/windows/desktop/api/Tom/nn-tom-itextrange2) se define mediante sus desplazamientos de posición de caracteres inicial y final y un objeto story. No existe independientemente de su objeto de caso principal, aunque su texto se puede copiar en el Portapapeles o en otros destinos. Un objeto de intervalo de texto es diferente de la hoja de cálculo y otros objetos de intervalo, que se definen mediante otros tipos de desplazamientos; por ejemplo, fila/columna o posición de gráficos (x, y). Un objeto de intervalo de texto puede modificarse de varias maneras, puede devolver un duplicado de sí mismo y se le puede enviar un comando para copiar sus posiciones de carácter inicial y final y su puntero de historia a la selección actual.

No se necesita un objeto de caso explícito, ya que siempre se puede crear un objeto [**ITextRange**](/windows/desktop/api/Tom/nn-tom-itextrange) para representar un caso determinado. En concreto, el objeto [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) puede crear un objeto [**ITextStoryRanges**](/windows/desktop/api/Tom/nn-tom-itextstoryranges) para enumerar los casos del documento en términos de intervalos con valores de posición de carácter inicial y final que describen casos completos (por ejemplo, 0 y **tomForward).**

Con un [**objeto ITextStoryRanges2,**](/windows/desktop/api/Tom/nn-tom-itextstoryranges2) no se necesita un objeto de historia explícito, ya que cada caso se describe mediante un [**objeto ITextRange2.**](/windows/desktop/api/Tom/nn-tom-itextrange2) En concreto, el objeto [**ITextDocument2**](/windows/desktop/api/tom/nn-tom-itextdocument2) puede crear un objeto [**ITextStoryRanges2**](/windows/desktop/api/tom/nn-tom-itextstoryranges2) para enumerar los casos del documento en términos de intervalos con valores de posición de carácter inicial y final que describen casos completos (por ejemplo, 0 y **tomForward).**

La [**interfaz ITextRow**](/windows/desktop/api/Tom/nn-tom-itextrow) junto con los métodos [**ITextRange::Move**](/windows/desktop/api/Tom/nf-tom-itextrange-move) e [**ITextRange::Expand**](/windows/desktop/api/Tom/nf-tom-itextrange-expand) ofrece la capacidad de insertar, consultar y cambiar tablas.

## <a name="tom-interface-conventions"></a>Convenciones de interfaz TOM

Todos los métodos TOM **devuelven valores HRESULT.** En general, los métodos TOM devuelven los siguientes valores estándar.

-   E \_ OUTOFMEMORY
-   E \_ INVALIDARG
-   E \_ NOTIMPL
-   E \_ FILENOTFOUND
-   E \_ ACCESSDENIED
-   E \_ FAIL
-   CO \_ E \_ RELEASED
-   NOERROR (igual que S \_ OK)
-   S \_ FALSE

Tenga en cuenta que si se elimina la instancia de edición asociada a un objeto TOM como [**ITextRange,**](/windows/desktop/api/Tom/nn-tom-itextrange) el objeto TOM deja de ser útil y todos sus métodos devuelven CO \_ E \_ RELEASED.

Además de los valores **devueltos de HRESULT,** muchos métodos incluyen parámetros out, que son punteros que se usan para devolver valores. Para todas las interfaces, debe comprobar todos los parámetros de puntero para asegurarse de que son distintos de cero antes de usarlos. Si pasa un valor NULL a un método que requiere un puntero válido, el método devuelve E \_ INVALIDARG. Se omiten los punteros out opcionales con valores NULL.

Use métodos con los prefijos Get y Set para obtener y establecer propiedades. Las variables **booleanas usan tomFalse** (0) para **FALSE** y **tomTrue** (-1) para **TRUE.**

Las constantes TOM se definen en el tipo de enumeración [**tomConstants**](/windows/win32/api/tom/ne-tom-tomconstants) y comienzan con el prefijo *tom*, por ejemplo **tomWord**.

## <a name="the-tombool-type"></a>El tipo tomBool

Muchos métodos TOM usan un tipo especial de variable denominado "tomBool" para atributos de texto enriquecido que tienen estados binarios. El tipo tomBool es diferente del **tipo booleano** porque puede tomar cuatro valores: **tomTrue**, **tomFalse,** **tomToggle** y **tomUndefined.** Los **valores tomTrue** **y tomFalse** indican true y false. El **valor tomToggle** se usa para alternar una propiedad. El **valor tomUndefined,** más tradicionalmente denominado NINCH, es un valor especial sin entrada y sin cambios que funciona con longs, floats y **COLORREF** s. Para las cadenas, **tomUndefined** (o NINCH) se representa mediante la cadena null. Para las operaciones de configuración de propiedades, **el uso de tomUndefined** no cambia la propiedad de destino. Para las operaciones de obtención de propiedades, **tomUndefined** significa que los caracteres del intervalo tienen valores diferentes (proporciona la casilla atenuada en los cuadros de diálogo de propiedades).

## <a name="math-buildup-and-build-down"></a>Compilación matemática y compilación

Puede usar el método [**ITextRange2::BuildUpMath**](/windows/desktop/api/Tom/nf-tom-itextrange2-buildupmath) para convertir expresiones matemáticas con formato lineal en versiones integradas. El [**método ITextRange2::Linearize**](/windows/desktop/api/Tom/nf-tom-itextrange2-linearize) realiza la conversión opuesta, denominada linearización o compilación, para volver a convertir las versiones integradas de expresiones matemáticas al formato lineal. La funcionalidad de compilación de cálculo matemático es útil cuando necesita exportar texto sin formato o habilitar determinados tipos de edición.

## <a name="tom-rtf"></a>TOM RTF

En TOM, el intercambio de texto enriquecido se puede realizar mediante conjuntos de llamadas a métodos explícitos o mediante transferencias de texto enriquecido en el formato de texto enriquecido (RTF). En esta sección se proporciona tablas de palabras de control RTF para las propiedades de párrafo y para las propiedades de caracteres.

**Palabras de control de párrafo TOM RTF**

| Palabra de control   | Significado                                                                                                                                                                                                                                                                        |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \\ fi *n*      | Sangría de primera línea (el valor predeterminado es cero).                                                                                                                                                                                                                                       |
| \\ Mantener        | Mantenga intacto el párrafo.                                                                                                                                                                                                                                                         |
| \\ keepn       | Siga con el párrafo siguiente.                                                                                                                                                                                                                                                  |
| \\ li *n*      | Sangría izquierda (el valor predeterminado es cero).                                                                                                                                                                                                                                             |
| \\ noline      | Sin numeración de líneas.                                                                                                                                                                                                                                                             |
| \\ nowidctlpar | Desactive el control huérfano o huérfano.                                                                                                                                                                                                                                                 |
| \\ pagebb      | Página de interrupción antes del párrafo.                                                                                                                                                                                                                                                   |
| \\ par         | Nuevo párrafo.                                                                                                                                                                                                                                                                 |
| \\ Pard        | Restablece las propiedades de párrafo predeterminadas.                                                                                                                                                                                                                                        |
| \\ Ql          | Alineado a la izquierda (valor predeterminado).                                                                                                                                                                                                                                                    |
| \\ Qr          | Alineado a la derecha.                                                                                                                                                                                                                                                                 |
| \\ Qj          | Justificado.                                                                                                                                                                                                                                                                     |
| \\ Qc          | Centrado.                                                                                                                                                                                                                                                                      |
| \\ ri *n*      | Sangría derecha (el valor predeterminado es cero).                                                                                                                                                                                                                                            |
| \\ s *n*       | Estilo *n*.                                                                                                                                                                                                                                                                     |
| \\ sa *n*      | Espacio después (el valor predeterminado es cero).                                                                                                                                                                                                                                             |
| \\ sb *n*      | Espacio anterior (el valor predeterminado es cero).                                                                                                                                                                                                                                            |
| \\ sl *n*      | Si falta o *si n*=1000, el espaciado de línea viene determinado por el carácter más alto de la línea (espaciado de una sola línea); si *n>* cero, se usa al menos este tamaño; si *n* es < cero, se \| *usa exactamente n.* \| El espaciado de línea es espaciado de varias líneas \\ si sigue slmult 1. |
| \\ slmult *m*  | Sigue \\ a sl. *m* = cero: al menos o exactamente el espaciado de línea tal y como se describe \\ en sl *n*. *m* = 1: espaciado de línea = *n*/240 veces espaciado de una sola línea.                                                                                                                              |
| \\ tb *n*      | Posición de la pestaña de la barra, en twips, desde el margen izquierdo.                                                                                                                                                                                                                              |
| \\ tldot       | Puntos de líder de tabulación.                                                                                                                                                                                                                                                               |
| \\ tleq        | Signo igual de líder de tabulación.                                                                                                                                                                                                                                                         |
| \\ tlhyph      | Guiones del líder de tabulación.                                                                                                                                                                                                                                                            |
| \\ tlth        | Línea gruesa del líder de tabulación.                                                                                                                                                                                                                                                         |
| \\ tlul        | Subrayado del líder de tabulación.                                                                                                                                                                                                                                                          |
| \\ Tqc         | Pestaña centrada.                                                                                                                                                                                                                                                                  |
| \\ tqdec       | Pestaña Decimal.                                                                                                                                                                                                                                                                   |
| \\ tqr         | Pestaña Vaciar a la derecha.                                                                                                                                                                                                                                                               |
| \\ tx *n*      | Posición de tabulación, en twips, desde el margen izquierdo.                                                                                                                                                                                                                                  |



 

**Palabras de control de formato de caracteres TOM RTF**

| Palabra de control     | Significado                                                                                                                                                                                                                                  |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \\ animación *n* | Establece el tipo de animación en *n*.                                                                                                                                                                                                              |
| \\ B             | Negrita.                                                                                                                                                                                                                                    |
| \\ Casquillos          | Todas las mayúsculas.                                                                                                                                                                                                                            |
| \\ cf *n*        | Color de primer plano (el valor predeterminado **es tomAutocolor).**                                                                                                                                                                                      |
| \\ cs *n*        | Estilo de *caracteres n*.                                                                                                                                                                                                                     |
| \\ dn *n*        | Posición de subíndice en puntos medio (el valor predeterminado es 6).                                                                                                                                                                                    |
| \\ Embo          | Relieve.                                                                                                                                                                                                                                |
| \\ f *n*         | Número de fuente, *n* hace referencia a una entrada de la tabla de fuentes.                                                                                                                                                                                   |
| \\ fs *n*        | Tamaño de fuente en puntos medio (el valor predeterminado es 24).                                                                                                                                                                                            |
| \\ highlight *n* | Color de fondo (el valor predeterminado **es tomAutocolor).**                                                                                                                                                                                      |
| \\ i             | Cursiva.                                                                                                                                                                                                                                  |
| \\ impr          | Impresión.                                                                                                                                                                                                                                 |
| \\ lang *n*      | Aplica un idioma a un carácter. *n* es un número que corresponde a un idioma. La \\ palabra de control sin formato restablece la propiedad language al idioma definido por \\ deflang *n* en las propiedades del documento.                             |
| \\ nosupersub    | Desactiva el superíndice o subíndice.                                                                                                                                                                                                      |
| \\ outl          | Contorno.                                                                                                                                                                                                                                 |
| \\ Llano         | Restablece las propiedades de formato de caracteres a un valor predeterminado definido por la aplicación. También se restablecen las propiedades de formato de caracteres asociadas (descritas en la sección Propiedades de caracteres asociados en la especificación RTF). |
| \\ scaps         | Mayúsculas pequeñas.                                                                                                                                                                                                                          |
| \\ Shad          | Sombra.                                                                                                                                                                                                                                  |
| \\ Huelga        | Tachado.                                                                                                                                                                                                                           |
| \\ Sub           | Aplica el subíndice al texto y reduce el tamaño del punto según la información de fuente.                                                                                                                                                          |
| \\ fenomenal         | Aplica el superíndice al texto y reduce el tamaño de punto según la información de fuente.                                                                                                                                                        |
| \\ Ul            | Subrayado continuo. \\ ul0 desactiva todas las sublines.                                                                                                                                                                                  |
| \\ Uld           | Subrayado con puntos.                                                                                                                                                                                                                        |
| \\ uldb          | Subrayado doble.                                                                                                                                                                                                                        |
| \\ ulnone        | Detiene todas las sublines.                                                                                                                                                                                                                   |
| \\ ulw           | Subrayado de palabras.                                                                                                                                                                                                                          |
| \\ up *n*        | Posición de superíndice en puntos medio (el valor predeterminado es 6).                                                                                                                                                                                  |
| \\ V             | Texto oculto.                                                                                                                                                                                                                             |



 

## <a name="finding-rich-text"></a>Buscar texto enriquecido

Puede usar métodos TOM para buscar texto enriquecido tal como se define en un intervalo de texto. Encontrar texto enriquecido exactamente es necesario a menudo en el procesamiento de palabras, aunque nunca se ha cumplido en un procesador de palabras "lo que se ve es lo que se obtiene" (WYSIWYG). Hay claramente un dominio mayor de coincidencia de texto enriquecido que permite omitir algunas propiedades de formato de caracteres (o incluir formato de párrafo o contenido de objeto), pero estas generalizaciones están fuera del ámbito de esta sección.

Un propósito de esta funcionalidad es  usar un cuadro de diálogo Buscar de texto enriquecido para definir el texto enriquecido que desea buscar en un documento. El cuadro de diálogo se implementaría mediante un control de edición enriquecido y los métodos TOM se usarían para llevar a cabo la búsqueda a través del documento. Puede copiar el texto enriquecido deseado del  documento en el cuadro de diálogo Buscar o escribirlo y dar formato directamente en el cuadro **de** diálogo Buscar.

En el ejemplo siguiente se muestra cómo usar métodos TOM para buscar texto que contenga combinaciones de formato de caracteres exactos. El algoritmo busca el texto sin formato en el intervalo de coincidencias, que se denomina `pr1` . Si se encuentra el texto sin formato, lo señala un intervalo de prueba, que se denomina `pr2` . A continuación, se usan dos intervalos de punto de inserción ( y ) para recorrer el intervalo de prueba comparando su formato de `prip1` caracteres con el de `prip2` `pr1` . Si coinciden exactamente, el intervalo de entrada (especificado por ) se actualiza para que apunte al texto del intervalo de prueba y la función devuelve el recuento de caracteres del `ppr` intervalo coincidente. En la comparación de formato de caracteres se usan dos objetos [**ITextFont,**](/windows/desktop/api/Tom/nn-tom-itextfont) y `pf1` `pf2` . Se adjuntan a los intervalos de punto de `prip1` inserción y `prip2` .


```
LONG FindRichText (
    ITextRange **ppr,             // Ptr to range to search
    ITextRange *pr1)              // Range with rich text to find
{
    BSTR        bstr;             // pr1 plain-text to search for
    LONG        cch;              // Text string count
    LONG        cch1, cch2;       // tomCharFormat run char counts
    LONG        cchMatch = 0;     // Nothing matched yet
    LONG        cp;               // Handy char position
    LONG        cpFirst1;         // pr1 cpFirst
    LONG        cpFirst2;         // pr2 cpFirst
    ITextFont  *    pf1, *pf      // Fonts corresponding to IPs prip1 and prip2
    ITextRange *pr2;              // Range duplicate to search with
    ITextRange *prip1, *prip      // Insertion points to walk pr1, pr2

    if (!ppr || !*ppr || !pr1)
        return E_INVALIDARG;

    // Initialize range and font objects used in search
    if ((*ppr)->GetDuplicate(&pr2)    != NOERROR ||
        pr1->GetDuplicate(&prip1)     != NOERROR ||
        pr2->GetDuplicate(&prip2)     != NOERROR ||
        prip1->GetFont(&pf1)          != NOERROR ||
        prip2->GetFont(&pf2)          != NOERROR ||
        pr1->GetText(&bstr)           != NOERROR )
    {
        return E_OUTOFMEMORY;
    }

    pr1->GetStart(&cpFirst1);

    // Keep searching till rich text is matched or no more plain-text hits
    while(!cchMatch && pr2->FindText(bstr, tomForward, 0, &cch) == NOERROR)
    {
        pr2->GetStart(&cpFirst2);                 // pr2 is a new trial range
        prip1->SetRange(cpFirst1, cpFirst1);      // Set up IPs to scan match
        prip2->SetRange(cpFirst2, cpFirst2);      //  and trial ranges

        while(cch > 0 &&
            pf1->IsEqual(pf2, NULL) == NOERROR)   // Walk match & trial ranges
        {                                         //  together comparing font
            prip1->GetStart(&cch1);               //  properties
            prip1->Move(tomCharFormat, 1, NULL);
            prip1->GetStart(&cp);
            cch1 = cp - cch1;                     // cch of next match font run

            prip2->GetStart(&cch2);
            prip2->Move(tomCharFormat, 1, NULL);
            prip2->GetStart(&cp);
            cch2 = cp - cch2;                      // cch of next trial font run

            if(cch1 < cch)                         // There is more to compare
            {
                if(cch1 != cch2)                   // Different run lengths:
                    break;                         //  no formatting match
                cch = cch - cch1;                  // Matched format run
            }
            else if(cch2 < cch)                    // Trial range format run too
                break;                             //  short

            else                                   // Both match and trial runs
            {                                      //  reach at least to match
                pr2->GetEnd(&cp);                  //  text end: rich-text match
                (*ppr)->SetRange(cpFirst2, cp)     // Set input range to hit
                cchMatch = cp - cpFirst2;          //  coordinates and return
                break;                             //  length of matched string
            }
        }
    }
    pr2->Release();
    prip1->Release();
    prip2->Release();
    pf1->Release();
    pf2->Release();
    SysFreeString(bstr);

    return cchMatch;
}
```



## <a name="tom-accessibility"></a>Accesibilidad de TOM

TOM proporciona compatibilidad de accesibilidad a través de las interfaces [**ITextSelection**](/windows/desktop/api/Tom/nn-tom-itextselection) [**e ITextRange.**](/windows/desktop/api/Tom/nn-tom-itextrange) En esta sección se describen los métodos que son útiles para la accesibilidad, así como cómo un programa puede determinar la posición de pantalla *x* e *y* de un objeto.

Dado que los programas de accesibilidad basados en la interfaz de usuario normalmente funcionan con la pantalla y el mouse, una preocupación común es encontrar la interfaz [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) correspondiente para la ubicación actual del mouse (en coordenadas de pantalla). En las secciones siguientes se presentan dos maneras de determinar la interfaz adecuada:

-   [A través de la tabla running-object](#interface-from-running-object-table)
-   A través [**del mensaje EM \_ GETOLEINTERFACE,**](em-getoleinterface.md) que funciona para instancias de edición enriquecciones en ventanas, siempre que el cliente esté en el mismo espacio de proceso *(no* se necesita serialización)

Para más información, consulte la especificación Microsoft Active Accessibility datos. Después de obtener un objeto desde una posición de pantalla, puede usar para una interfaz [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) y llamar al [**método RangeFromPoint**](/windows/desktop/api/Tom/nf-tom-itextdocument-rangefrompoint) para obtener un objeto de intervalo vacío en la cp correspondiente a la posición de la pantalla.

### <a name="interface-from-running-object-table"></a>Interfaz de la tabla de objetos en ejecución

Una tabla de objetos en ejecución (ROT) indica qué instancias de objeto están activas. Al consultar esta tabla, puede acelerar el proceso de conexión de un cliente a un objeto cuando el objeto ya se está ejecutando. Para que los programas puedan acceder a las interfaces TOM a través de la tabla de objetos en ejecución, una instancia de TOM con una ventana debe registrarse en ROT mediante un moniker. El moniker se construye a partir de una cadena que contiene el valor hexadecimal de su [**HWND.**](/windows/desktop/WinProg/windows-data-types) En el ejemplo de código siguiente se muestra cómo hacerlo.


```
// This TOM implementation code is executed when a new windowed 
// instance starts up. 
// Variables with leading underscores are members of this class.

HRESULT hr;
OLECHAR szBuf[10];            // Place to put moniker
MONIKER *pmk;

hr = StringCchPrintf(szBuff, 10, "%x", _hwnd);
if (FAILED(hr))
{
    //
    // TODO: write error handler
    //
}
CreateFileMoniker(szBuf, &pmk);
OleStdRegisterAsRunning(this, pmk, &_dwROTcookie);
....................
 
// Accessibility Client: 
//    Find hwnd for window pointed to by mouse cursor.

GetCursorPos(&pt);
hwnd = WindowFromPoint(pt);

// Look in ROT (running object table) for an object attached to hwnd

hr = StringCchPrintf(szBuff, 10, "%x", hwnd);
if (FAILED(hr))
{
    //
    // TODO: write error handler
    //
}
CreateFileMoniker(szBuf, &pmk);
CreateBindContext(0, &pbc);
pmk->BindToObject(pbc, NULL, IID_ITextDocument, &pDoc);
pbc->Release();

if( pDoc )
{
    pDoc->RangeFromPoint(pt.x, pt.y, &pRange);
    // ...now do whatever with the range pRange
}
```



### <a name="interface-from-window-messages"></a>Interfaz de mensajes de ventana

El [**mensaje EM \_ GETOLEINTERFACE**](em-getoleinterface.md) proporciona otra manera de obtener una [**interfaz IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) para un objeto en una posición de pantalla determinada. Como se describe [en Interfaz de la tabla de](#interface-from-running-object-table)objetos en ejecución , obtiene un [**HWND**](/windows/desktop/WinProg/windows-data-types) para la posición de la pantalla y, a continuación, envía este mensaje a ese **HWND.** El **mensaje EM \_ GETOLEINTERFACE** es específico de edición enriquecido y devuelve un puntero a una [**interfaz IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) en la variable que *dirige lParam*.

**Sugerencia** Si se devuelve un puntero (asegúrese de establecer el objeto al que *lParam* apunta a NULL antes de enviar el mensaje), puede llamar a su método [**IUnknown::QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obtener una [**interfaz ITextDocument.**](/windows/desktop/api/Tom/nn-tom-itextdocument) En el ejemplo de código siguiente se muestra este método.


```
    HWND    hwnd;
    ITextDocument *pDoc;
    ITextRange *pRange;
    POINT    pt;
    IUnknown *pUnk = NULL;
    
    GetCursorPos(&pt);
    hwnd = WindowFromPoint(pt);
    SendMessage(hwnd, EM_GETOLEINTERFACE, 0, (LPARAM)&pUnk);
    if(pUnk && 
        pUnk->QueryInterface(IID_ITextDocument, &pDoc) == NOERROR)
    {
        pDoc->RangeFromPoint(pt.x, pt.y, &pRange);
        //  ... continue with rest of program
    }
```



### <a name="accessibility-oriented-methods"></a>Métodos orientados a la accesibilidad

Algunos métodos TOM son especialmente útiles para navegar por la pantalla, mientras que otros métodos TOM mejoran lo que puede hacer cuando llega a lugares de interés. En la tabla siguiente se describen los métodos más útiles.



| Método                                                 | Cómo promueve la accesibilidad                                                                                                                                                                 |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetSelection**](/windows/desktop/api/Tom/nf-tom-itextdocument-getselection)     | Este método obtiene la selección activa que se puede usar para una variedad de propósitos orientados a la vista, como resaltar texto y desplazarse.                                                      |
| [**RangeFromPoint**](/windows/desktop/api/Tom/nf-tom-itextdocument-rangefrompoint) | Cuando se usa en una selección activa, se garantiza que este método obtiene un intervalo asociado a una vista determinada.                                                                                 |
| [**Expanda**](/windows/desktop/api/Tom/nf-tom-itextrange-expand)                    | Amplía un intervalo de texto para que todas las unidades parciales que contiene estén completamente contenidas. Por ejemplo, `Expand(tomWindow)` expande el intervalo para incluir la parte visible de la historia del intervalo. |
| [**GetDuplicate**](/windows/desktop/api/Tom/nf-tom-itextrange-getduplicate)        | Cuando se usa en una selección activa, se garantiza que este método obtiene un intervalo asociado a una vista determinada. Vea la descripción de [**RangeFromPoint.**](/windows/desktop/api/Tom/nf-tom-itextdocument-rangefrompoint)  |
| [**GetPoint**](/windows/desktop/api/Tom/nf-tom-itextrange-getpoint)                | Obtiene las coordenadas de pantalla para la posición del carácter inicial o final en el intervalo de texto.                                                                                                        |
| [**ScrollIntoView**](/windows/desktop/api/Tom/nf-tom-itextrange-scrollintoview)    | Desplaza un intervalo de texto a la vista.                                                                                                                                                               |
| [**Ajuste**](/windows/desktop/api/Tom/nf-tom-itextrange-setpoint)                | Selecciona texto en o hacia arriba a través de un punto especificado.                                                                                                                                              |



 

## <a name="character-match-sets"></a>Juegos de coincidencias de caracteres

El *parámetro variant* de los distintos métodos **Move** de \* [**ITextRange,**](/windows/desktop/api/Tom/nn-tom-itextrange)como [**MoveWhile**](/windows/desktop/api/Tom/nf-tom-itextrange-movewhile) y [**MoveUntil**](/windows/desktop/api/Tom/nf-tom-itextrange-moveuntil), puede tomar una cadena explícita o un índice de 32 bits de juego de coincidencia de caracteres. Los índices se definen mediante intervalos Unicode o conjuntos [**de caracteres GetStringTypeEx.**](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw) El intervalo Unicode a partir de *n* y de longitud *l* (< 32768) se especifica mediante el índice *n* + (*l <*< 16) + 0x80000000. Por ejemplo, las letras básicas de griego se definen mediante CR Griego = 0x805f0370 caracteres ASCII imprimibles se definen mediante \_ CR \_ ASCIIPrint = 0x805e0020. Además, los métodos **MoveWhile** y **MoveUntil** permiten omitir rápidamente un intervalo de caracteres en cualquier juego de caracteres **GetStringTypeEx** o en un intervalo de caracteres que no está en ninguno de estos juegos de caracteres.

Los [**conjuntos GetStringTypeEx**](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw) se especifican mediante los valores de *Ctype1,* *Ctype2* y *Ctype3,* y se definen de la siguiente manera.



| Cset                 | Significado                          |
|----------------------|----------------------------------|
| *Ctype1*             | Combinación de tipos \_ CTYPE1 de CT. |
| *Ctype2* + tomCType2 | Cualquier tipo \_ CTYPE2 ct.             |
| *Ctype3* + tomCType3 | Combinación de tipos \_ CTYPE3 de CT. |



 

En concreto, *Ctype1* puede ser cualquier combinación de lo siguiente.



| Nombre de Ctype1 | Value  | Significado                                                           |
|-------------|--------|-------------------------------------------------------------------|
| C1 \_ UPPER   | 0x0001 | Mayúsculas.                                                        |
| C1 \_ LOWER   | 0x0002 | Minúsculas.                                                        |
| DÍGITO \_ C1   | 0x0004 | Dígitos decimales.                                                   |
| ESPACIO \_ C1   | 0x0008 | Caracteres de espacio.                                                 |
| C1 \_ PUNCT   | 0x0010 | La puntuación.                                                      |
| C1 \_ CNTRL   | 0x0020 | Caracteres de control.                                               |
| C1 \_ BLANK   | 0x0040 | Caracteres en blanco.                                                 |
| C1 \_ XDIGIT  | 0x0080 | Dígitos hexadecimales.                                               |
| C1 \_ ALPHA   | 0x0100 | Cualquier carácter lingüístico (alfabético, silabario o ideográfico). |
| C1 \_ DEFINIDO | 0x0200 | Carácter definido, pero no uno de los otros tipos \_ \* C1.       |



 

Los *tipos Ctype2* admiten el diseño adecuado del texto Unicode. Los atributos de dirección se asignan para que el algoritmo de diseño bidireccional estandarizado por Unicode produzca resultados precisos. Estos tipos son mutuamente excluyentes. Para obtener más información sobre el uso de estos atributos, vea *The Unicode Standard: Worldwide Character Encoding, Volumes 1 and 2*, Addison-Wesley Publishing Company: 1991, 1992.



| Nombre de CType2          | Value | Significado                          |
|----------------------|-------|----------------------------------|
| Fuerte:              |       |                                  |
| C2 \_ LEFTTORIGHT      | 0x1   | De izquierda a derecha.                   |
| C2 \_ RIGHTTOLEFT      | 0x2   | De derecha a izquierda.                   |
| Débil:                |       |                                  |
| C2 \_ EUROPENUMBER     | 0x3   | Número europeo, dígito europeo. |
| C2 \_ EUROPESEPARATOR  | 0x4   | Separador numérico europeo.      |
| C2 \_ EUROPETERMINATOR | 0x5   | Terminador numérico europeo.     |
| C2 \_ ARABICNUMBER     | 0x6   | Número árabe.                   |
| C2 \_ COMMONSEPARATOR  | 0x7   | Separador numérico común.        |
| Neutral:             |       |                                  |
| C2 \_ BLOCKSEPARATOR   | 0x8   | Separador de bloques.                 |
| C2 \_ SEGMENTSEPARATOR | 0x9   | Separador de segmentos.               |
| C2 \_ WHITESPACE       | 0xA   | Espacio en blanco.                     |
| C2 \_ OTHERNEUTRAL     | 0xB   | Otros neutros.                  |
| No aplicable:      |       |                                  |
| C2 \_ NOTAPPLICABLE    | 0x0   | Sin dirección implícita.           |



 

Los *tipos Ctype3 están* diseñados para ser marcadores de posición para las extensiones de los tipos POSIX necesarios para el procesamiento de texto general o para las funciones estándar de la biblioteca de C.



| Nombre de CType3       | Value  | Significado                                                             |
|-------------------|--------|---------------------------------------------------------------------|
| C3 \_ NONSPACING    | 0x1    | Marca que no está en elpacing.                                                    |
| C3 \_ DIACRITIC     | 0x2    | Marca de no espacio diacrítica.                                          |
| C3 \_ VOWELMARK     | 0x4    | Marca de no apacing de vowel.                                              |
| SÍMBOLO \_ C3        | 0x8    | Símbolo.                                                             |
| C3 \_ KATAKANA      | 0x10   | Carácter Katakana.                                                 |
| C3 \_ HIRAGANA      | 0x20   | Carácter hiragana.                                                 |
| C3 \_ HALFWIDTH     | 0x40   | Carácter de ancho medio.                                               |
| C3 \_ FULLWIDTH     | 0x80   | Carácter de ancho completo.                                               |
| C3 \_ IDEOGRAPH     | 0x100  | Carácter ideográfico.                                              |
| C3 \_ KASHIDA       | 0x200  | Carácter Kashida árabe.                                           |
| C3 \_ ALPHA         | 0x8000 | Todos los caracteres lingüísticos (alfabético, silabario e ideográfico). |
| C3 \_ NOTAPPLICABLE | 0x0    | No aplicable.                                                     |



 

Un Kit de desarrollo de edición (EDK) podría incluir definiciones de índice *pVar* para los siguientes intervalos descritos en el estándar Unicode.



| Juego de caracteres         | Intervalo Unicode | Juego de caracteres             | Intervalo Unicode |
|-----------------------|---------------|---------------------------|---------------|
| ASCII                 | 0x0: 0x7f      | ANSI                      | 0x0: 0xff      |
| ASCIIPrint            | 0x20: 0x7e     | Latin1                    | 0x20: 0xff     |
| Latin1Supp            | 0xa0: 0xff     | LatinXA                   | 0x100: 0x17f   |
| LatinXB               | 0x180: 0x24f   | IPAX                      | 0x250: 0x2af   |
| SpaceMod              | 0x2b0: 0x2ff   | Combinar                 | 0x300: 0x36f   |
| Griego                 | 0x370: 0x3ff   | BasicGreek                | 0x370: 0x3cf   |
| GriegoSímboles          | 0x3d0: 0x3ff   | Cirílico                  | 0x400: 0x4ff   |
| Armenio              | 0x530: 0x58f   | Hebreo                    | 0x590: 0x5ff   |
| BasicHebrew           | 0x5d0: 0x5ea   | HebrewXA                  | 0x590: 0x5cf   |
| HebreoXB              | 0x5eb: 0x5ff   | Árabe                    | 0x600: 0x6ff   |
| BasicArabic           | 0x600: 0x652   | ArabicX                   | 0x653: 0x6ff   |
| Devangari             | 0x900: 0x97f   | Bangla (anteriormente Jadei) | 0x980: 0x9ff   |
| Gurmukhi              | 0xa00: 0xa7f   | Gujarati                  | 0xa80: 0xaff   |
| Seia (anteriormente Oriya) | 0xb00: 0xb7f   | Tamil                     | 0xb80: 0xbff   |
| Telgada                | 0xc00: 0xc7f   | Canarés                   | 0xc80: 0xcff   |
| Malayalam             | 0xd00: 0xd7f   | Tailandés                      | 0xe00: 0xe7f   |
| Lao                   | 0xe80: 0xeff   | HexadecimalX                 | 0x10a0: 0xa0cf |
| BascGeorgian          | 0x10d0: 0x10ff | Jamo                      | 0x1100: 0x11ff |
| LatinXAdd             | 0x1e00: 0x1eff | GreekX                    | 0x1f00: 0x1fff |
| GenPunct              | 0x2000: 0x206f | Superscript               | 0x2070: 0x207f |
| Subscript             | 0x2080: 0x208f | SuperSubscript            | 0x2070: 0x209f |
| Moneda              | 0x20a0: 0x20cf | CombMarkSym               | 0x20d0: 0x20ff |
| LetterLike            | 0x2100: 0x214f | NumberForms               | 0x2150: 0x218f |
| Flechas                | 0x2190: 0x21ff | MathOps                   | 0x2200: 0x22ff |
| MiscTech              | 0x2300: 0x23ff | CtrlPictures              | 0x2400: 0x243f |
| OptCharRecog          | 0x2440: 0x245f | EnclAlphaNum              | 0x2460: x24ff  |
| BoxDrawing            | 0x2500: 0x257f | BlockElement              | 0x2580: 0x259f |
| GeometShapes          | 0x25a0: 0x25ff | MiscSymbols               | 0x2600: 0x26ff |
| Dingbats              | 0x2700: 0x27bf | CJKSymPunct               | 0x3000: 0x303f |
| Hiragana              | 0x3040: 0x309f | Katakana                  | 0x30a0: 0x30ff |
| Bopomofo              | 0x3100: 0x312f | HangulJamo                | 0x3130: 0x318f |
| CLIGMisc               | 0x3190: 0x319f | EnclCJK                   | 0x3200: 0x32ff |
| CJKCompatibl          | 0x3300: 0x33ff | Han                       | 0x3400: 0xabff |
| Hangul                | 0xac00: 0xd7ff | UTF16Lead                 | 0xd800: 0xdbff |
| UTF16Trail            | 0xdc00: 0xdfff | PrivateUse                | 0xe000: 0xf800 |
| CJKCompIdeog          | 0xf900: 0xfaff | AlphaPres                 | 0xfb00: 0xfb4f |
| ArabicPresA           | 0xfb50: 0xfdff | CombHalfMark              | 0xfe20: 0xfe2f |
| CJKCompForm           | 0xfe30: 0xfe4f | SmallFormVar              | 0xfe50: 0xfe6f |
| ArabicPresB           | 0xfe70: 0xfefe | HalfFullForm              | 0xff00: 0xffef |
| Especiales              | 0xfff0: 0xfffd |                           |               |



 

 

 