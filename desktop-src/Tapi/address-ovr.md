---
description: El concepto de una dirección es el núcleo de la mayoría de las operaciones de comunicaciones.
ms.assetid: 32fbd06b-f6f2-4024-b8d5-3d6eef16bca2
title: Dirección
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c6ad8f03b725a58d564c63f4c5c0d0165eed99a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678126"
---
# <a name="address"></a>Dirección

El concepto de una dirección es el núcleo de la mayoría de las operaciones de comunicaciones. Una dirección representa una ubicación en una red. La asignación local de una dirección a una línea o canal normalmente tiene lugar durante la instalación del proveedor de servicios, pero se puede modificar más adelante. Puede encontrar detalles sobre los procedimientos implicados en el kit de recursos del sistema operativo para los proveedores de servicios proporcionados por Microsoft y en la documentación del proveedor de servicios para productos que no sean de Microsoft.

Una sola dirección puede compartirse por más de un dispositivo de línea. Distintos proveedores de conmutadores tienen nombres diferentes para este concepto, como el puente de direcciones, el número de directorio de varios aspectos (MADN) o la apariencia de puente. Una llamada entrante en una dirección compartida se ofrece en todas las líneas asociadas a la dirección. Vea [ \_ constantes LINEADDRESSSHARING](./lineaddresssharing--constants.md) para obtener una descripción de las configuraciones que TAPI reconoce.

La propia dirección es una cadena que identifica una ubicación en una red. En el caso de una red telefónica, la dirección es un número de teléfono completo con códigos nacionales o internacionales. Si la red está basada en IP, la dirección puede ser una dirección IP. Vea [LINEADDRESSTYPE \_ constantes](lineaddresstype--constants.md) for TAPI-Defined Address Types. Un proveedor de servicios puede definir tipos de direcciones adicionales.

## <a name="address-related-capabilities-and-messages"></a>Address-Related funcionalidades y mensajes

Las distintas direcciones tienen características, capacidades y Estados diferentes. Los proveedores de servicios son el origen de esa información. La funcionalidad de consulta de dispositivos y el estado y los mecanismos de informes de eventos de TAPI proporcionan a una aplicación la información para administrar las direcciones.

Las aplicaciones adquieren esta información procesando eventos de TAPI o usando operaciones de consulta. Esto permite que una aplicación tenga en cuenta factores como, por ejemplo, si una determinada dirección admite una funcionalidad específica, como [Park](park-ovr.md).

**TAPI 2. x:** Las aplicaciones llaman a la función [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) para determinar las capacidades de telefonía de cada dirección y, a continuación, reciben esta información en una estructura de datos [**LINEADDRESSCAPS**](/windows/win32/api/tapi/ns-tapi-lineaddresscaps) . De forma similar, una aplicación puede llamar a [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) para un dispositivo de línea con el fin de determinar el número de direcciones asignado a la línea, así como otra información.

**TAPI 3. x:** Las aplicaciones utilizan las [interfaces de objeto de dirección](address-object-interfaces.md) para obtener información sobre las capacidades y los eventos de dirección.

## <a name="storing-phone-numbers-in-electronic-address-books"></a>Almacenar números de teléfono en las libretas de direcciones electrónicas

Muchos usuarios deciden marcar a personas, equipos de fax, tablones de anuncios y otras entidades seleccionando sus nombres en una libreta de direcciones. El número real marcado depende de la ubicación geográfica del usuario y el modo en que se conecta el dispositivo de línea que se va a usar. Por ejemplo, un equipo de escritorio puede tener acceso a dos líneas, una conectada a una PBX, la otra a la oficina central de la compañía telefónica. Al realizar una llamada a la misma entidad, es posible que se tengan que usar diferentes números. (Para marcar a través de la PBX, por ejemplo, es posible que el equipo tenga que marcar un prefijo "9" para obtener una línea externa, o puede que sea necesario un prefijo diferente para una llamada realizada a través de la oficina central). O bien, un usuario puede realizar llamadas desde un equipo portátil y desea utilizar una sola libreta de direcciones estáticas, incluso cuando se llama desde diferentes ubicaciones o entornos de telefonía. Las funcionalidades de traducción de direcciones de TAPI permiten al usuario informar al equipo de la ubicación actual y el dispositivo de línea deseado para la llamada. A continuación, TAPI controla cualquier diferencia de marcado, sin necesidad de realizar cambios en la libreta de direcciones del usuario. Una aplicación utiliza la [traducción de direcciones](initiate-a-session-ovr.md) para convertir una dirección del formato de [dirección canónico](#canonical-addresses) en el formato de [dirección de marcado](#dialable-addresses) .

Un tema relacionado es el control de la supervisión internacional del progreso de la llamada, que es el proceso de escuchar tonos auditivos como el tono de marcado, tonos de información especiales, señales ocupadas y tonos de timbre para determinar el *Estado* de una llamada (su progreso a través de la red). Dado que las cadencias y las frecuencias de los tonos de progreso de la llamada varían de país o región a país o región, el proveedor de servicios debe saber qué progreso de la llamada seguir al realizar una llamada de salida internacional. Por lo tanto, las aplicaciones especifican el código de país o región de destino al realizar llamadas salientes.

## <a name="canonical-addresses"></a>Direcciones canónicas

El formato de dirección canónico está pensado para ser un número de directorio constante universal. Por esta razón, los números de las libretas de direcciones se almacenan mejor con formato canónico.

Los detalles siguientes se refieren a lo que se considera canónico para una dirección de teléfono.

Una dirección de teléfono canónica es una cadena de texto con la siguiente estructura:

\+*CountryCode* Espacio \[ **(**_AreaCode_*_)_* espacio \] *númerodesuscriptor* \| nombre de *Subdirección*  ^   CRLF...

Los componentes de esta estructura se describen en la tabla siguiente.



Componente

Significado

\+

Equivalente a Hex 2B. Indica que el número que sigue usa el formato canónico.

*País*

Una cadena de tamaño de variable que contiene uno o varios de los dígitos "0" a "9" (Hex 30 a 39, inclusive). El *CountryCode* se delimita con el siguiente espacio. Identifica el país o región en el que se encuentra la dirección.

Space

Exactamente un carácter de espacio (hex 20). Se utiliza para delimitar el final de la parte del *CountryCode* de una dirección.

*Códigodeárea*

Una cadena de tamaño de variable que contiene cero o más dígitos de "0" a "9" (Hex 30 a 39, inclusive). *AreaCode* es la parte del código de área de la dirección y es opcional. Si el código de área está presente, debe ir precedido de un carácter de paréntesis de apertura (28) y debe ir seguido de exactamente un carácter de paréntesis de cierre (29) y un carácter de espacio (20).

*Númerodesuscriptor*

Una cadena de tamaño de variable que contiene uno o varios de los dígitos "0" a "9" (Hex 30 a 39, inclusive). También puede incluir otros caracteres de formato, incluidos los caracteres de control de marcado descritos en el formato de dirección de marcado:

 

Carácter

codificación hexadecimal

 

! \#<br/> $<br/> \*<br/> ,<br/> ?<br/> @<br/> ABCD<br/> P<br/> T<br/> W<br/> abcd<br/> p<br/> t<br/> w<br/>

21 23<br/> 24<br/> 2<br/> 2C<br/> 3F<br/> 40<br/> 41-44<br/> 50<br/> 54<br/> 77<br/> 61-64<br/> 70<br/> 74<br/> 79<br/>

 

El número de suscriptor no debe contener el paréntesis izquierdo o el carácter de paréntesis de cierre (que solo se usa para delimitar el código de área), ni debe contener los \| caracteres "", "^" o CRLF (que se usan para comenzar los campos siguientes). Normalmente, los caracteres que no son dígitos en el número de suscriptor solo incluirán espacios, puntos (".") y guiones ("-"). Los caracteres no dígitos permitidos que aparecen en el número de suscriptor se omiten del *DialableString* devuelto por la función [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) , pero se conservan en el *DisplayableString*.

\|

Hex (7C). Si este carácter opcional está presente, la información que le sigue hasta el siguiente carácter + \| ^ CRLF o el final de la cadena de dirección canónica se trata como información de Subdirección, como en el caso de una Subdirección ISDN (RDSI).

*Subdirección*

Una cadena de tamaño de variable que contiene una Subdirección. La cadena está delimitada por + \| ^ CRLF o el final de la cadena de dirección. Durante el marcado, se pasa información de Subdirección a la parte remota. Puede ser como una Subdirección ISDN (RDSI) o una dirección de correo electrónico.

^

Hex (5E). Si este carácter opcional está presente, la información que le sigue hasta el siguiente CRLF o el final de la cadena de dirección canónica se trata como un nombre ISDN (RDSI).

*Nombre*

Una cadena de tamaño de variable tratada como información de nombre. El nombre está delimitado por CRLF o el final de la cadena de dirección canónica y puede contener otros delimitadores. Durante el marcado, la información de nombre se pasa a la parte remota.

CRLF

Hex (0D) seguido de Hex (0A) y es opcional. Si está presente, indica que otro número canónico sigue a este. Se usa para separar varias direcciones canónicas como parte de una cadena de dirección única (multiplexación inversa). Por ejemplo, la representación canónica del número de teléfono principal del panel de activación en Microsoft Corporation sería:<br/> + 1 (425) 882-8080<br/>



 

## <a name="dialable-addresses"></a>Direcciones marcables

El formato de dirección de marcado es el formulario en el que se pasa una dirección a un proveedor de servicios que se encarga de los números de teléfono. Los detalles siguientes se refieren a las direcciones que se van a marcar en una red telefónica.

El formato de número de marcado permite que se proporcionen varias direcciones de destino a la vez. Esta capacidad puede ser útil si el proveedor de servicios ofrece algún tipo de multiplexación inversa mediante la configuración de llamadas a cada uno de los destinos especificados y, a continuación, la administración de la secuencia de información como una única secuencia multimedia de ancho de banda alto. La aplicación percibe este grupo de llamadas como una sola llamada, ya que solo recibe un identificador de llamada único que representa el agregado de las llamadas telefónicas individuales.

También es posible admitir multiplexación inversa en el nivel de aplicación. Para ello, la aplicación configuraría una serie de llamadas individuales y sincronizaría sus flujos multimedia.

La *Subdirección* es una funcionalidad que se proporciona en las líneas ISDN (RDSI) que permiten más información que un único número de teléfono que se va a usar al marcar. Esta información adicional puede especificar una extensión de teléfono individual para sonar o, en un entorno informático, una aplicación determinada que se va a notificar. Otros parámetros pueden describir los aspectos necesarios de una conexión solicitada, como la velocidad y el tiempo.

Si un proveedor de servicios admite la Subdirección, la aplicación lo incluye en la dirección que se pasa a cualquier operación que requiera una.

Una dirección telefónica marcada contiene información sobre el direccionamiento de partes y es parte de la navegación por la naturaleza. Se supone que cualquier cadena de entrada que no comienza con un carácter "+" está en formato canónico y, por tanto, está en formato de dirección de marcado y se devuelve a la aplicación sin modificar. Una dirección de marcado es una cadena de texto con la siguiente estructura:

*DialableNumber* \| *Subdirección*  ^  *Nombre* de CRLF...

Los componentes de esta estructura se proporcionan en la tabla siguiente.



| Componente        | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *DialableNumber* | Dígitos y modificadores 0-9 A-D \* \# ,! W p p p t @ $? ; delimitado por \| ^ CRLF o el final de la cadena de dirección de marcado. El signo más (+) es un carácter válido en las cadenas que se puede marcar. Indica que el número de teléfono es un número internacional completo. En *DialableNumber*, tenga en cuenta las siguientes definiciones:<br/> 0-9 a-D \*\#<br/> Caracteres correspondientes a los dígitos DTMF y/o pulsos.<br/> |
| !                | Hex (21). Indica que se va a insertar en la cadena de marcado un hookflash (un enlace de un segundo y un segundo, seguido de un OffHook de la segunda mitad del tiempo antes de continuar).                                                                                                                                                                                                                                                                                   |
| P p              | Hex (50) o hexadecimal (70). Indica que el marcado por pulsos se va a usar para los dígitos que hay a continuación.                                                                                                                                                                                                                                                                                                                                                |
| T t              | Hex (54) o hexadecimal (74). Indica que el marcado de tono (DTMF) se va a usar para los dígitos que hay a continuación.                                                                                                                                                                                                                                                                                                                                          |
| ,                | Hex (27). Indica que el marcado se va a pausar. La duración de una pausa es específica del dispositivo y se puede recuperar de las capacidades del dispositivo de la línea. Se pueden usar varias comas para proporcionar las pausas más largas.                                                                                                                                                                                                                                 |
| W              | Hex (57) o hexadecimal (77). Una letra mayúscula o minúscula W indica que el marcado debería continuar solo después de que se haya detectado un tono de marcado.                                                                                                                                                                                                                                                                                                            |
| @                | Hex (40). Indica que el marcado es "esperar la respuesta silenciosa" antes de marcar el resto de la dirección de marcado. Esto significa que debe esperar al menos un tono de timbre seguido de varios segundos de silencio.                                                                                                                                                                                                                               |
| $                | Hex (24). Indica que el marcado de la información de facturación está esperando una "señal de facturación" (por ejemplo, un tono de solicitud de tarjeta de crédito).                                                                                                                                                                                                                                                                                                              |
| ?                | Hex (3F). Indica que se debe preguntar al usuario antes de continuar con el marcado. En realidad, el proveedor no realiza la solicitud, pero la presencia de "?" obliga al proveedor a rechazar la cadena como no válida, avisando a la aplicación de la necesidad de dividirla en partes y preguntar al usuario entre ellas.                                                                                                                           |
| ;                | Hex (3B). Si se coloca al final de una cadena de dirección de marcado parcialmente especificada, indica que la información del número que se puede marcar está incompleta y se proporciona más información de dirección más adelante. El componente ";" solo se permite en la parte *DialableNumber* de una dirección.                                                                                                                                                       |
| \|               | Hex (7C) y es opcional. Si está presente, la información que le sigue hasta el siguiente carácter + \| ^ CRLF o el final de la cadena de dirección de marcado se trata como información de Subdirección (como para una Subdirección ISDN).                                                                                                                                                                                                                                  |
| *Subdirección*     | Una cadena de tamaño de variable que contiene una Subdirección. La cadena está delimitada por el siguiente carácter + \| ^ CRLF o el final de la cadena de dirección. Al marcar, se pasa información de Subdirección a la parte remota. Puede ser para una Subdirección ISDN, una dirección de correo electrónico, etc.                                                                                                                                                                       |
| ^                | Hex (5E) y es opcional. Si está presente, la información que le sigue hasta el siguiente CRLF o el final de la cadena de dirección de marcado se trata como un nombre ISDN (RDSI).                                                                                                                                                                                                                                                                                |
| *Nombre*           | Una cadena de tamaño de variable tratada como información de nombre. El nombre está delimitado por CRLF o el final de la cadena de dirección de marcado. Al marcar, se pasa la información de nombre a la parte remota.                                                                                                                                                                                                                                                      |
| CRLF             | Hex (0D) seguido de Hex (0A). Si está presente, este carácter opcional indica que otro número que se va a marcar sigue a este. Se usa para separar varias direcciones marcables como parte de una sola cadena de dirección (para multiplexación inversa).                                                                                                                                                                                           |



 

La traducción de direcciones se puede usar para traducir una dirección del formato canónico al formato de marcado.

 

