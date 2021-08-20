---
description: El concepto de una dirección es fundamental para la mayoría de las operaciones de comunicaciones.
ms.assetid: 32fbd06b-f6f2-4024-b8d5-3d6eef16bca2
title: Dirección
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a18285c0b15f0914935847ad7618de052762164f972c3f774ed838b4f8d10dbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117949191"
---
# <a name="address"></a>Dirección

El concepto de una dirección es fundamental para la mayoría de las operaciones de comunicaciones. Una dirección representa una ubicación en una red. La asignación local de una dirección a una línea o canal normalmente tiene lugar durante la instalación del proveedor de servicios, pero se puede modificar más adelante. Puede encontrar detalles sobre los procedimientos implicados en el Kit de recursos del sistema operativo para proveedores de servicios proporcionados por Microsoft y en la documentación del proveedor de servicios para productos que no son de Microsoft.

Más de un dispositivo de línea puede compartir una dirección única. Los distintos proveedores de modificadores tienen nombres diferentes para este concepto, como el puente de direcciones, el número de directorio de varias apariencias (MADN) o la apariencia puenteada. Se ofrece una llamada entrante en una dirección compartida en todas las líneas asociadas a la dirección. Consulte [LINEADDRESSSHARING \_ Constants (Constantes LINEADDRESSSHARING)](./lineaddresssharing--constants.md) para obtener una descripción de las configuraciones que TAPI reconoce.

La propia dirección es una cadena que identifica una ubicación en una red. En el caso de una red telefónica, la dirección es un número de teléfono completo con códigos nacionales o internacionales. Si la red está basada en IP, la dirección puede ser una dirección IP. Consulte [LineADDRESSTYPE \_ Constants for](lineaddresstype--constants.md) TAPI-defined address types (Constantes LINEADDRESSTYPE para tipos de direcciones definidos por TAPI). Un proveedor de servicios puede definir tipos de direcciones adicionales.

## <a name="address-related-capabilities-and-messages"></a>Address-Related funcionalidades y mensajes

Las distintas direcciones tienen características, funcionalidades y estados diferentes. Los proveedores de servicios son el origen de dicha información. La funcionalidad de consulta de dispositivos de TAPI, el estado y los mecanismos de informes de eventos proporciona a una aplicación la información para administrar direcciones.

Las aplicaciones adquieren esta información mediante el procesamiento de eventos de TAPI o mediante operaciones de consulta. Esto permite a una aplicación tener en cuenta factores como si una dirección determinada admite una funcionalidad específica, como [el aparcamiento](park-ovr.md).

**TAPI 2.x:** Las aplicaciones llaman a la función [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) para determinar las funcionalidades de telefonía de cada dirección y, a continuación, reciben esta información en una estructura de datos [**LINEADDRESSCAPS.**](/windows/win32/api/tapi/ns-tapi-lineaddresscaps) De forma similar, una aplicación puede llamar a [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) para que un dispositivo de línea determine el número de direcciones asignadas a la línea, así como otra información.

**TAPI 3.x:** Las aplicaciones usan las [interfaces de objeto de dirección](address-object-interfaces.md) para adquirir información sobre las funcionalidades y los eventos de dirección.

## <a name="storing-phone-numbers-in-electronic-address-books"></a>Almacenamiento de Teléfono en libretas de direcciones electrónicas

Muchos usuarios eligen marcar a personas, máquinas de fax, paneles de boletín y otras entidades seleccionando sus nombres en una libreta de direcciones. El número real marcado depende de la ubicación geográfica del usuario y de la forma en que se conecta el dispositivo de línea que se va a usar. Por ejemplo, un equipo de escritorio puede tener acceso a dos líneas, una conectada a una HORA ÚNICA y la otra a la oficina central de la empresa telefónica. Al realizar una llamada a la misma entidad, puede que deban usarse números diferentes. (Para marcar a través de LAN, por ejemplo, es posible que el equipo tenga que marcar un prefijo "9" para obtener una línea externa o que se necesite un prefijo diferente para una llamada realizada a través de la oficina central). O bien, un usuario puede realizar llamadas desde un equipo portátil y desea usar una única libreta de direcciones estática incluso cuando se llama desde diferentes ubicaciones o entornos de telefonía. Las funcionalidades de traducción de direcciones de TAPI permiten al usuario informar al equipo de la ubicación actual y del dispositivo de línea deseado para la llamada. TAPI controla las diferencias de marcación, sin necesidad de realizar ningún cambio en la libreta de direcciones del usuario. Una aplicación usa [la traducción de direcciones](initiate-a-session-ovr.md) para convertir una dirección del formato de dirección [canónica](#canonical-addresses) al formato de dirección que se [puede marcar.](#dialable-addresses)

Un tema relacionado es el control de la supervisión internacional del progreso de las llamadas, que es el proceso de escucha de  los tonos acústicos, como el tono de marcado, los tono de información especial, las señales ocupadas y los tonos de anillo para determinar el estado de una llamada (su progreso a través de la red). Dado que las cadencias y frecuencias de los tonos de progreso de llamada varían de país o región a país o región, el proveedor de servicios debe saber qué progreso de llamada debe seguir al realizar una llamada saliente internacional. Por lo tanto, las aplicaciones especifican el código de país o región de destino al realizar llamadas salientes.

## <a name="canonical-addresses"></a>Direcciones canónicas

El formato de dirección canónica está pensado para ser un número de directorio constante universal. Por este motivo, los números de las libretas de direcciones se almacenan mejor con formato canónico.

Los detalles siguientes se refieren a lo que se considera canónico para una dirección telefónica.

Una dirección de teléfono canónica es una cadena de texto con la siguiente estructura:

\+*CountryCode* Space \[ **(**_AreaCode_*_)_* Space \] *SubscriberNumber* \| *Subaddress*  ^  *Name* CRLF ...

Los componentes de esta estructura se describen en la tabla siguiente.



Componente

Significado

\+

Equivalente a hexadecimal 2B. Indica que el número siguiente usa el formato canónico.

*CountryCode*

Cadena de tamaño variable que contiene uno o varios de los dígitos "0" a "9" (hexadecimal del 30 al 39, ambos inclusive). *CountryCode* está delimitado por el siguiente espacio. Identifica el país o región en el que se encuentra la dirección.

Space

Exactamente un carácter de espacio (hexadecimal 20). Se usa para delimitar el final de la parte *CountryCode* de una dirección.

*AreaCode*

Cadena de tamaño variable que contiene cero o más de los dígitos "0" a "9" (hexadecimal del 30 al 39, ambos inclusive). *AreaCode* es la parte del código de área de la dirección y es opcional. Si el código de área está presente, debe ir precedido exactamente de un carácter de paréntesis izquierdo (28) y seguido exactamente de un carácter de paréntesis derecho (29) y un carácter de espacio (20).

*SubscriberNumber*

Cadena de tamaño variable que contiene uno o varios de los dígitos "0" a "9" (hexadecimal del 30 al 39, ambos inclusive). También puede incluir otros caracteres de formato, incluidos cualquiera de los caracteres de control de marcado que se describen en el formato de dirección que se puede marcar:

 

Carácter

codificación hexadecimal

 

! \#<br/> $<br/> \*<br/> ,<br/> ?<br/> @<br/> Abcd<br/> P<br/> T<br/> W<br/> abcd<br/> p<br/> t<br/> w<br/>

21 23<br/> 24<br/> 2A<br/> 2c<br/> 3f<br/> 40<br/> 41-44<br/> 50<br/> 54<br/> 77<br/> 61-64<br/> 70<br/> 74<br/> 79<br/>

 

El número de suscriptor no debe contener el paréntesis izquierdo ni el carácter de paréntesis derecho (que solo se usan para delimitar el código de área), ni debe contener los caracteres ", "^" o CRLF (que se usan para comenzar los campos \| siguientes). Normalmente, los caracteres nondigit en el número de suscriptor solo incluirían espacios, puntos (".") y guiones ("-"). Los caracteres nondigit permitidos que aparecen en el número de suscriptor se omiten de *dialableString* devueltos por la función [**lineTranslateAddress,**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) pero se conservan en *DisplayableString*.

\|

Hexadecimal (7C). Si este carácter opcional está presente, la información siguiente hasta el siguiente + ^ CRLF, o el final de la cadena de dirección canónica, se trata como información de subdirección, como para una subdirección \| ISDN.

*Subdirección*

Cadena de tamaño variable que contiene una subdirección. La cadena está delimitada por + \| ^ CRLF o el final de la cadena de dirección. Durante la marcación, la información de la subdirección se pasa a la entidad remota. Puede ser algo como una subdirección ISDN o una dirección de correo electrónico.

^

Hexadecimal (5E). Si este carácter opcional está presente, la información siguiente hasta el siguiente CRLF o el final de la cadena de dirección canónica se trata como un nombre ISDN.

*Nombre*

Cadena de tamaño variable que se trata como información de nombre. El nombre está delimitado por CRLF o el final de la cadena de dirección canónica y puede contener otros delimitadores. Durante la marcación, la información de nombre se pasa a la entidad remota.

CRLF

Hexadecimal (0D) seguido de Hexadecimal (0A) y es opcional. Si está presente, indica que otro número canónico sigue a este. Se usa para separar varias direcciones canónicas como parte de una sola cadena de dirección (multiplexación inversa). Por ejemplo, la representación canónica del número de teléfono de la placa de conmutación principal en Microsoft Corporation sería:<br/> +1 (425) 882-8080<br/>



 

## <a name="dialable-addresses"></a>Direcciones que se pueden marcar

El formato de dirección que se puede marcar es el formulario en el que se pasa una dirección a un proveedor de servicios que controla los números de teléfono. Los detalles siguientes se refieren a las direcciones que se pueden marcar en una red telefónica.

El formato de número que se puede marcar permite proporcionar varias direcciones de destino a la vez. Esta capacidad puede ser útil si el proveedor de servicios ofrece algún tipo de multiplexación inversa configurando llamadas a cada uno de los destinos especificados y, a continuación, administrando el flujo de información como un único flujo multimedia de ancho de banda alto. La aplicación percibe este grupo de llamadas como una sola llamada porque recibe solo un identificador de llamada que representa el agregado de las llamadas telefónicas individuales.

También es posible admitir la multiplexación inversa en el nivel de aplicación. Para ello, la aplicación configuraría una serie de llamadas individuales y sincronizaría sus transmisiones multimedia.

*La subdirección* es una funcionalidad que se proporciona en las líneas de ISDN que permite usar más información que un solo número de teléfono al marcar. Esta información adicional puede especificar una extensión telefónica individual para llamar a o, en un entorno informático, una aplicación determinada a la que se va a alertar. Otros parámetros pueden describir los aspectos necesarios de una conexión solicitada, como la velocidad y el tiempo.

Si un proveedor de servicios admite la subdirección, la aplicación la incluye en la dirección que se pasa a cualquier operación que requiera una.

Una dirección telefónica que se puede marcar contiene información de direccionamiento de parte y es parte de navegación por naturaleza. Se supone que cualquier cadena de entrada que no comience con un carácter "+" no esté en formato canónico y, por tanto, esté en formato de dirección que se puede marcar, y se devuelve a la aplicación sin modificar. Una dirección que se puede marcar es una cadena de texto con la siguiente estructura:

*DialableNumber* \| *Subaddress*  ^  *Nombre* Crlf...

Los componentes de esta estructura se dan en la tabla siguiente.



| Componente        | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *DialableNumber* | Dígitos y modificadores 0-9 A-D \* \# , ! W w P p T t @ $ ? ; delimitado por \| ^ CRLF o el final de la cadena de dirección que se puede marcar. El signo más (+) es un carácter válido en cadenas que se pueden marcar. Indica que el número de teléfono es un número internacional completo. En *DialableNumber*, tenga en cuenta las definiciones siguientes:<br/> 0-9 D \*\#<br/> Caracteres correspondientes a los dígitos DTMF o pulse.<br/> |
| !                | Hexadecimal (21). Indica que se va a insertar un hookflash (un onhook de medio segundo seguido de un offhook de medio segundo antes de continuar) en la cadena de marcado.                                                                                                                                                                                                                                                                                   |
| P p              | Hexadecimal (50) o hexadecimal (70). Indica que la marcación de pulsación se va a usar para los dígitos siguientes.                                                                                                                                                                                                                                                                                                                                                |
| T t              | Hexadecimal (54) o hexadecimal (74). Indica que la marcación de tono (DTMF) se va a usar para los dígitos siguientes.                                                                                                                                                                                                                                                                                                                                          |
| ,                | Hexadecimal (27). Indica que se va a pausar la marcación. La duración de una pausa es específica del dispositivo y se puede recuperar de las funcionalidades del dispositivo de la línea. Se pueden usar varias comas para proporcionar pausas más largas.                                                                                                                                                                                                                                 |
| W w              | Hexadecimal (57) o hexadecimal (77). Un W en mayúsculas o minúsculas indica que la marcación solo debe continuar después de que se haya detectado un tono de marcado.                                                                                                                                                                                                                                                                                                            |
| @                | Hexadecimal (40). Indica que la marcación es "esperar una respuesta silenciosa" antes de marcar el resto de la dirección que se puede marcar. Esto significa esperar al menos un tono de anillo seguido de varios segundos de silencio.                                                                                                                                                                                                                               |
| $                | Hexadecimal (24). Indica que marcar la información de facturación es esperar una "señal de facturación" (por ejemplo, un tono de aviso de tarjeta de crédito).                                                                                                                                                                                                                                                                                                              |
| ?                | Hexadecimal (3F). Indica que se va a solicitar al usuario antes de continuar con la marcación. El proveedor no realiza realmente la solicitud, pero la presencia de "?" obliga al proveedor a rechazar la cadena como no válida, lo que alerta a la aplicación de la necesidad de dividirla en partes y preguntar al usuario entre ellos.                                                                                                                           |
| ;                | Hexadecimal (3B). Si se coloca al final de una cadena de dirección que se puede marcar parcialmente, indica que la información del número de marcado está incompleta y se proporciona más información de dirección más adelante. El componente ";" solo se permite en la *parte DialableNumber* de una dirección.                                                                                                                                                       |
| \|               | Hexadecimal (7C) y es opcional. Si está presente, la información siguiente hasta el siguiente + ^ CRLF, o el final de la cadena de dirección que se puede marcar se trata como información de subdirección (como para una subdirección \| ISDN).                                                                                                                                                                                                                                  |
| *Subdirección*     | Cadena de tamaño variable que contiene una subdirección. La cadena está delimitada por el siguiente + \| ^ CRLF o el final de la cadena de dirección. Al marcar, la información de subdirección se pasa a la entidad remota. Puede ser para una subdirección ISDN, una dirección de correo electrónico, y así sucesivamente.                                                                                                                                                                       |
| ^                | Hexadecimal (5E) y es opcional. Si está presente, la información siguiente hasta el siguiente CRLF o el final de la cadena de dirección que se puede marcar se trata como un nombre ISDN.                                                                                                                                                                                                                                                                                |
| *Nombre*           | Cadena de tamaño variable que se trata como información de nombre. El nombre está delimitado por CRLF o el final de la cadena de dirección que se puede marcar. Al marcar, la información de nombre se pasa a la entidad remota.                                                                                                                                                                                                                                                      |
| CRLF             | Hexadecimal (0D) seguido de Hexadecimal (0A). Si está presente, este carácter opcional indica que otro número que se puede marcar sigue a este. Se usa para separar varias direcciones que se pueden marcar como parte de una sola cadena de dirección (para multiplexación inversa).                                                                                                                                                                                           |



 

La traducción de direcciones se puede usar para traducir una dirección del formato canónico al formato que se puede marcar.

 

