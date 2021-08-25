---
description: El Panel de entrada de Microsoft Tablet PC es una herramienta eficaz para escribir texto manuscrito con un lápiz y corregir texto sin usar un teclado.
ms.assetid: c45ac1b5-7713-4bcb-a130-4692cff99aa2
title: Habilitación de la corrección de texto para los recopiladores de lápiz personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: accb0bf2129a4e93e543e3ec5cc73d3e65383dc57b581114f30e812b1ac88b8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940839"
---
# <a name="enabling-text-correction-for-custom-ink-collectors"></a>Habilitación de la corrección de texto para los recopiladores de lápiz personalizados

El Panel de entrada de Microsoft Tablet PC es una herramienta eficaz para escribir texto manuscrito con un lápiz y corregir texto sin usar un teclado. Al usar el Panel de entrada, un usuario escribe texto escribiendo a mano en las superficies de entrada de entrada, lo que hace que el Panel de entrada reconozca la escritura a mano del usuario como texto. Una vez que se ha reconocido el texto, el usuario pulsa Insertar en el Panel de entrada para insertar el texto en una aplicación o documento. Antes de insertar el texto, un usuario tiene acceso a un conjunto de herramientas de corrección en el Panel de entrada. Entre ellas se incluye la selección de un resultado de reconocimiento alternativo, la capacidad de reescribir un solo carácter o incluso de rascar toda la palabra y reescribir. Estas herramientas de corrección permiten al usuario corregir errores de reconocimiento y humanos.

Una vez que el texto especificado mediante el Panel de entrada está en el documento, los usuarios tienen acceso a la misma funcionalidad de corrección que está disponible antes de la inserción en aplicaciones basadas en Windows [Text Services Framework](/windows/desktop/TSF/text-services-framework)y habilitadas para Text Services. A partir de Microsoft Windows XP Service Pack 2 Tablet PC Edition, todas las aplicaciones rich edit están habilitadas para Text Services de forma predeterminada y, a partir de Windows Vista, las aplicaciones HTML están habilitadas para Text Services de forma predeterminada. La corrección en el documento solo está disponible en aplicaciones basadas y habilitadas en Text Service. Esto se debe a que el Panel de entrada depende de la capacidad de Text Service para almacenar las propiedades de texto asociadas, incluidos los objetos de entrada de lápiz y las alternativas de reconocimiento, con el fin de proporcionar corrección en el documento.

![Panel de entrada de tablet PC con corrección de texto](images/a0dced5e-16de-410b-965f-5d97d297cee5.jpg)

Sin embargo, hay numerosos escenarios, como la corrección del reconocimiento de voz o la corrección de texto escrito sobre la marcha, que no comienzan con la entrada de texto mediante el Panel de entrada, pero en los que la corrección en el documento puede ser muy útil para los usuarios de Tabletas PC. Un ejemplo excelente es en las aplicaciones que proporcionan superficies de entrada de entrada personalizadas para escribir texto mediante un lápiz. Las superficies de entrada de entrada personalizadas son una excelente manera de que las aplicaciones proporcionen una funcionalidad única y personalizada específica para las tareas de entrada de texto de cada aplicación. Además, las superficies de entrada de entrada personalizadas proporcionan una experiencia de usuario de Tablet PC totalmente integrada, lo que deja claro que el lápiz es un dispositivo de entrada de primera clase en aplicaciones que las contienen. Sin embargo, es posible que las aplicaciones que proporcionan superficies de entrada de entrada personalizadas no permitan o no puedan proporcionar el mismo nivel de compatibilidad con la corrección que está disponible en la corrección en el documento del Panel de entrada.

![recopilador de entrada de lápiz personalizado](images/b6797b12-dda6-44c4-87f4-570fe0c23f3a.jpg)

Las aplicaciones basadas o habilitadas en Text Services en las que la corrección en el documento es útil para la corrección del texto no especificado mediante el Panel de entrada pueden usar la API [**IHandWrittenTextInsertion del**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) Panel de entrada [(clase Microsoft.TextInput.HandwrittenTextInsertion](/previous-versions/ms573516(v=vs.100)) en código administrado) para habilitar la corrección en el documento para el texto escrito por otros medios. De esta manera, las aplicaciones pueden agregar de forma económica una eficaz compatibilidad con correcciones a sus superficies de entrada de entrada de texto personalizadas u otros escenarios de entrada de texto, y redondear su historia de entrada de texto de Tablet PC. La API IHandWrittenTextInsertion del panel de entrada se incluye como parte del sistema operativo Windows Vista y como parte del SDK de la plataforma de tableta versión 1.9 o posterior. Se incluye una versión basada en .NET y COM de la API. La habilitación de la corrección en el documento para el texto no especificado mediante el Panel de entrada se admite en Windows Vista y versiones más recientes. La corrección en el documento solo está disponible para idiomas latinos y no puede mostrar ningún carácter fuera del juego de caracteres latinos.

## <a name="how-to-use-the-handwrittentextinsertion-api-in-an-application"></a>Uso de la API HandwrittenTextInsertion en una aplicación

Los cambios necesarios en una aplicación para integrar la corrección en el documento del Panel de entrada para el texto no especificado mediante el Panel de entrada y el uso de la API [**IHandWrittenTextInsertion**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) son sencillos. Todo el código de entrada de texto personalizado de la aplicación permanece sin cambios, excepto en el último paso. En el momento en que el texto especificado mediante una superficie de entrada manuscrita personalizada, el reconocimiento de voz u otros medios se va a mostrar en un campo de texto habilitado para servicios de texto, la aplicación envía el texto a la interfaz **IHandWrittenTextInsertion** en lugar de enviarlo directamente al campo de texto. A continuación, el componente de programación panel de entrada controla la inserción del texto en el campo de texto y el almacén de respaldo de Text Services. Al agregar el texto al almacén de respaldo de Text Services, el componente de programación panel de entrada controla el establecimiento de las propiedades de texto necesarias para que la corrección en el documento esté habilitada para ese texto.

En la sección siguiente se explica detalladamente este proceso para una aplicación de C++ mediante la versión COM de la API [**IHandWrittenTextInsertion.**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) Hay notas en cualquier lugar en las que los pasos para usar la .NET Framework de la API en C difieren en el uso de \# la versión COM en C++. La API **HandwrittenTextInsertion** administrada incluye una única interfaz COM, **IHandwrittenTextInsertion.** La definición de esta interfaz se encuentra en PenInputPanel.h y PenInputPanel \_ i.c.

En primer lugar, la aplicación debe usar la función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para generar una instancia de [**IHandWrittenTextInsertion**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) con el identificador de clase **CLSID \_ HandwrittenTextInsertion**. Tenga en cuenta que la creación de un objeto **\_ HandwrittenTextInsertion de CLSID** solo se realizará correctamente después de crear una ventana y de que se le haya dado el foco, porque hasta entonces no se activa el almacén de respaldo de Text Services. Además, si tiptsf.dll está presente en el sistema, se produce un error en la función **CoCreateInstance** y devuelve **REGDB \_ E \_ CLASSNOTREG**, lo que indica que la corrección en el documento del Panel de entrada no se admite en el sistema. En este momento, la aplicación debe continuar sin intentar habilitar la corrección del panel de entrada en el documento. La instancia de **HandwrittenTextInsertion** debe ser accesible desde el código de la aplicación que controla la inserción de texto en un campo de texto.

> [!Note]  
> Al trabajar con la versión .NET Framework de la API, la aplicación debe agregar una instrucción using para permitir el acceso al espacio de nombres [Microsoft.Ink.TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)) y, a continuación, crear el objeto directamente.

 

En segundo lugar, el código de la aplicación responsable de insertar texto en un campo de texto debe modificarse para que ya no inserte texto en un campo de texto directamente, sino que llame a uno u otro de los dos métodos de inserción de [**IHandwrittenTextInsertion**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion)en su lugar. Si las aplicaciones deben elegir llamar a [**InsertRecognitionResultsArray**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ihandwrittentextinsertion-insertrecognitionresultsarray) o [**InsertRecognitionResults**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ihandwrittentextinsertion-insertinkrecognitionresult) depende de si la aplicación tiene las alternativas de reconocimiento para el texto almacenado como una matriz o como un objeto [**IInkRecognitionResult.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)

> [!Note]  
> Cuando se trabaja en código administrado, el objeto de reconocimiento correspondiente consumido por InsertRecognitionResultsArray es [RecognitionResult.](/previous-versions/ms552537(v=vs.100)) Ambos métodos consumen los tres parámetros siguientes:

 

-   *alternates* Es una colección bidimensional de cadenas, almacenada como una matriz de matrices o como un [**objeto IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) (o [RecognitionResult).](/previous-versions/ms552537(v=vs.100)) Si las alternativas se almacenan como una matriz de matrices, se debe pasar como un puntero de matriz seguro. Cada entrada de la matriz de nivel superior es una lista de alternativas para una sola palabra en la inserción. La entrada en la posición cero de las submatriz de alternativas es el texto que se inserta en el campo de texto. Las alternativas adicionales (índices del 1 al n en cada submatriz) se almacenan en el almacén de respaldo de Text Services y se ofrecen al usuario como opciones como parte de la corrección en el documento. Si no se incluyen alternativas, el usuario ve "No suggestion" en lugar de la lista de alternativas. Si una inserción contiene varias palabras con espacios entre ellas, cada espacio debe incluirse como una entrada en la matriz de nivel superior.
-   *idioma* LcID de idioma [de entrada](/previous-versions/ms221397(v=vs.71)) que corresponde al texto contenido en el *parámetro alternates.* En el caso de que el contenido de las *alternativas* se generara mediante un reconocedor de escritura a mano o voz, esta es también la propiedad [**Languages**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) asociada al reconocedor usado.
-   *fLatticeContainsAutoSpacingInformation* Marca que indica si un reconocedor generó el texto contenido en el parámetro *alternates* con el espaciado automático habilitado. Si se ha habilitado el espaciado automático, la marca debe establecerse en **TRUE.** Si se deshabilitó el espaciado automático, la marca debe establecerse en **FALSE.** En el caso en el que el contenido de las *alternativas* lo generó un reconocedor que no admite el espaciado automático o no lo generó ningún reconocedor, la marca debe establecerse en **FALSE.**

El modelo de programación del Panel de entrada puede insertar el texto en el documento o la aplicación desde la posición del elemento de inserción del sistema.

Ambos métodos **devuelven S \_ OK** si la inserción se realiza correctamente. Devuelven **E \_ NOINTERFACE** si la aplicación no está basada o habilitada en Text Services, y **E \_ INVALIDARG** si *las alternativas* tienen un formato incorrecto o son inaccesibles. También pueden devolver **E \_ OUTOFMEMORY** si no hay suficiente memoria disponible en el sistema o **E \_ FAIL** después de un error catastrófico, como el Text Services Framework no está habilitado.

### <a name="conclusion"></a>Conclusión

Habilitar la corrección en el documento del Panel de entrada para el texto que no se ha escrito mediante el Panel de entrada es una manera sencilla y económica para que una aplicación basada o habilitada en Text Services complemente un método de entrada o entrada de entrada personalizado con una eficaz funcionalidad de corrección basada en lápiz. En Windows Vista, todas las aplicaciones Rich Edit y Trident están habilitadas para Text Services. Aunque las superficies de entrada de entrada integradas son una excelente opción para agregar una experiencia de usuario personalizada de Tablet PC a una aplicación, solo admiten la mitad de la entrada de texto si no incluyen funcionalidades de corrección. La corrección en el documento proporciona a los usuarios la otra mitad del caso agregando la capacidad de intercambiar una selección por una alternativa de reconocimiento, o de volver a escribir parte o toda la selección.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programar el panel de entrada de texto](programming-the-text-input-panel.md)
</dt> </dl>

 

 
