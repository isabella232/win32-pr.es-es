---
description: Enumera los valores devueltos por las funciones en las API de autenticación.
ms.assetid: ea519e5c-98b0-4a01-b2cc-e5ff736a5396
title: Valores devueltos de autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce618e906bedd1834b0a10ad7569e691034d8071f156c0182e6505fa8444578d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141398"
---
# <a name="authentication-return-values"></a>Valores devueltos de autenticación

## <a name="network-provider-values"></a>Valores del proveedor de red

La [API del proveedor de red](network-provider-api.md) usa los siguientes valores definidos.



| Value                                                                           | Descripción                                               |
|---------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Valores devueltos de seguridad de red](network-security-return-values.md)<br/> | Devuelve valores que un proveedor de red puede establecer.<br/> |



 

## <a name="smart-card-return-values"></a>Valores devueltos de tarjeta inteligente

[Las funciones de tarjeta](authentication-functions.md) inteligente devuelven los siguientes valores devueltos. Estos valores devueltos se definen en Scarderr.h.

> [!Note]  
> Algunos valores devueltos pueden tener el mismo valor que los valores Windows valores devueltos que significan una condición similar. Para obtener información sobre los códigos de error que no aparecen aquí, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

 



| Value                                                               | Descripción                                                                                                                                                                                                 |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ERROR \_ DE CANALIZACIÓN \_ ROTA<br/> 0x00000109<br/>                | El cliente intentó una operación de tarjeta inteligente en una sesión remota, como una sesión de cliente que se ejecuta en un servidor terminal, y el sistema operativo en uso no admite el redireccionamiento de tarjetas inteligentes.<br/> |
| SCARD \_ E \_ BAD \_ SEEK<br/> 0x80100029<br/>                | Error al establecer el puntero de objeto de archivo de tarjeta inteligente.<br/>                                                                                                                                 |
| SCARD \_ E \_ CANCELLED<br/> 0x80100002<br/>                | Una solicitud [**SCardCancel**](/windows/desktop/api/Winscard/nf-winscard-scardcancel) canceló la acción.<br/>                                                                                                                        |
| SCARD \_ E \_ CANT \_ DISPOSE<br/> 0x8010000E<br/>            | El sistema no pudo eliminar los medios de la manera solicitada.<br/>                                                                                                                               |
| TARJETA SCARD \_ E \_ NO \_ ADMITIDA<br/> 0x8010001C<br/>        | La tarjeta inteligente no cumple los requisitos mínimos de soporte técnico.<br/>                                                                                                                                   |
| CERTIFICADO SCARD \_ E \_ NO \_ DISPONIBLE<br/> 0x8010002D<br/> | No se pudo obtener el certificado solicitado.<br/>                                                                                                                                                 |
| SCARD \_ E \_ COMM \_ DATA \_ LOST<br/> 0x8010002F<br/>         | Se ha detectado un error de comunicaciones con la tarjeta inteligente. <br/>                                                                                                                                   |
| SCARD \_ E \_ DIR \_ NOT \_ FOUND<br/> 0x80100023<br/>          | El directorio especificado no existe en la tarjeta inteligente.<br/>                                                                                                                                        |
| LECTOR DUPLICADO \_ DE SCARD E \_ \_<br/> 0x8010001B<br/>        | El [*controlador del*](/windows/desktop/SecGloss/r-gly) lector no produjo un nombre de lector único.<br/>                                                                            |
| NO SE \_ ENCONTRÓ EL ARCHIVO SCARD \_ \_ \_ E<br/> 0x80100024<br/>         | El archivo especificado no existe en la tarjeta inteligente.<br/>                                                                                                                                             |
| SCARD \_ E \_ ICC \_ CREATEORDER<br/> 0x80100021<br/>         | No se admite el orden solicitado de creación de objetos.<br/>                                                                                                                                         |
| INSTALACIÓN DE SCARD \_ E \_ ICC \_<br/> 0x80100020<br/>        | No se encuentra ningún proveedor principal para la tarjeta inteligente.<br/>                                                                                                                                             |
| BÚFER INSUFICIENTE \_ DE SCARD E \_ \_<br/> 0x80100008<br/>     | El búfer de datos para los datos devueltos es demasiado pequeño para los datos devueltos.<br/>                                                                                                                            |
| SCARD \_ E \_ INVALID \_ ATR<br/> 0x80100015<br/>             | Una [*cadena ATR*](/windows/desktop/SecGloss/a-gly) obtenida del Registro no es una cadena ATR válida.<br/>                                                        |
| SCARD \_ E \_ CHV NO \_ VÁLIDO<br/> 0x8010002A<br/>             | El PIN proporcionado es incorrecto.<br/>                                                                                                                                                                   |
| IDENTIFICADOR NO \_ VÁLIDO DE SCARD E \_ \_<br/> 0x80100003<br/>          | El identificador proporcionado no era válido.<br/>                                                                                                                                                               |
| SCARD \_ E \_ INVALID \_ PARAMETER<br/> 0x80100004<br/>       | Uno o varios de los parámetros proporcionados no se pudieron interpretar correctamente.<br/>                                                                                                                        |
| DESTINO NO VÁLIDO DE SCARD \_ E \_ \_<br/> 0x80100005<br/>          | Falta información de inicio del Registro o no es válida.<br/>                                                                                                                                            |
| SCARD \_ E VALOR NO \_ \_ VÁLIDO<br/> 0x80100011<br/>           | Uno o varios de los valores de parámetro proporcionados no se pudieron interpretar correctamente.<br/>                                                                                                                  |
| SCARD \_ E \_ NO \_ ACCESS<br/> 0x80100027<br/>               | Se deniega el acceso al archivo.<br/>                                                                                                                                                                    |
| SCARD \_ E \_ NO \_ DIR<br/> 0x80100025<br/>                  | La ruta de acceso proporcionada no representa un directorio de tarjeta inteligente.<br/>                                                                                                                                     |
| SCARD \_ E \_ NO \_ FILE<br/> 0x80100026<br/>                 | La ruta de acceso proporcionada no representa un archivo de tarjeta inteligente.<br/>                                                                                                                                          |
| SCARD \_ E \_ NO \_ KEY \_ CONTAINER<br/> 0x80100030<br/>       | El contenedor de claves solicitado no existe en la tarjeta inteligente.<br/>                                                                                                                                    |
| SCARD \_ E \_ NO \_ MEMORY<br/> 0x80100006<br/>               | No hay suficiente memoria disponible para completar este comando.<br/>                                                                                                                                            |
| SCARD \_ E \_ NO \_ PIN \_ CACHE<br/> 0x80100033<br/>           | El PIN de tarjeta inteligente no se puede almacenar en caché.<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Este código de error no está disponible.<br/> <br/>                        |
| SCARD \_ E \_ NO \_ READERS \_ AVAILABLE<br/> 0x8010002E<br/>   | No hay ningún lector de tarjetas inteligentes disponible.<br/>                                                                                                                                                               |
| SCARD \_ E \_ NO \_ SERVICE<br/> 0x8010001D<br/>              | El administrador de [*recursos de tarjeta inteligente*](/windows/desktop/SecGloss/r-gly) no se está ejecutando.<br/>                                                                |
| SCARD \_ E \_ NO \_ SMARTCARD<br/> 0x8010000C<br/>            | La operación requiere una tarjeta inteligente, pero actualmente no hay ninguna tarjeta inteligente en el dispositivo.<br/>                                                                                                               |
| SCARD \_ E \_ NO \_ SUCH \_ CERTIFICATE<br/> 0x8010002C<br/>    | El certificado solicitado no existe.<br/>                                                                                                                                                        |
| SCARD \_ E \_ NOT \_ READY<br/> 0x80100010<br/>               | El lector o la tarjeta no está listo para aceptar comandos.<br/>                                                                                                                                              |
| SCARD \_ E \_ NOT \_ TRANSACTED<br/> 0x80100016<br/>          | Se intentó finalizar una transacción inexistente.<br/>                                                                                                                                            |
| SCARD \_ E \_ PCI \_ TOO \_ SMALL<br/> 0x80100019<br/>          | El búfer de recepción pci era demasiado pequeño.<br/>                                                                                                                                                            |
| LA CACHÉ DE PIN \_ DE SCARD E \_ \_ \_ EXPIRÓ<br/> 0x80100032<br/>      | La memoria caché del PIN de tarjeta inteligente ha expirado.<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Este código de error no está disponible.<br/> <br/>                       |
| ERROR DE COINCIDENCIA DE PROTO DE SCARD \_ E \_ \_<br/> 0x8010000F<br/>          | Los protocolos solicitados no son compatibles con el protocolo actualmente en uso con la tarjeta.<br/>                                                                                                       |
| TARJETA SCARD \_ E \_ DE SOLO \_ \_ LECTURA<br/> 0x80100034<br/>         | La tarjeta inteligente es de solo lectura y no se puede escribir en .<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Este código de error no está disponible.<br/> <br/>       |
| LECTOR E \_ SCARD \_ NO \_ DISPONIBLE<br/> 0x80100017<br/>      | El lector especificado no está disponible actualmente para su uso.<br/>                                                                                                                                         |
| LECTOR \_ SCARD E \_ \_ NO COMPATIBLE<br/> 0x8010001A<br/>      | El controlador de lector no cumple los requisitos mínimos de soporte técnico.<br/>                                                                                                                                |
| SERVIDOR SCARD \_ E \_ DEMASIADO \_ \_ OCUPADO<br/> 0x80100031<br/>        | El administrador de recursos de tarjeta inteligente está demasiado ocupado para completar esta operación.<br/>                                                                                                                          |
| SCARD \_ E \_ SERVICE \_ STOPPED<br/> 0x8010001E<br/>         | El administrador de recursos de tarjeta inteligente se ha apagado.<br/>                                                                                                                                                   |
| INFRACCIÓN DE \_ USO COMPARTIDO DE SCARD E \_ \_<br/> 0x8010000B<br/>       | No se puede acceder a la tarjeta inteligente debido a otras conexiones pendientes.<br/>                                                                                                                      |
| SCARD \_ E \_ SYSTEM \_ CANCELLED<br/> 0x80100012<br/>        | El sistema canceló la acción, presumiblemente para cerrarla o cerrarla.<br/>                                                                                                                       |
| SCARD \_ E \_ TIMEOUT<br/> 0x8010000A<br/>                  | El valor de tiempo de espera especificado por el usuario ha expirado.<br/>                                                                                                                                                   |
| SCARD \_ E \_ UNEXPECTED<br/> 0x8010001F<br/>               | Se ha producido un error inesperado en la tarjeta.<br/>                                                                                                                                                           |
| TARJETA DESCONOCIDA \_ SCARD E \_ \_<br/> 0x8010000D<br/>            | No se reconoce el nombre de tarjeta inteligente especificado.<br/>                                                                                                                                                 |
| LECTOR DESCONOCIDO DE SCARD \_ E \_ \_<br/> 0x80100009<br/>          | No se reconoce el nombre de lector especificado.<br/>                                                                                                                                                     |
| SCARD \_ E \_ UNKNOWN \_ RES \_ MNG<br/> 0x8010002B<br/>        | Se devolvió un código de error desconocido.<br/>                                                                                                                                                         |
| CARACTERÍSTICA NO ADMITIDA DE SCARD \_ E \_ \_<br/> 0x80100022<br/>     | Esta tarjeta inteligente no admite la característica solicitada.<br/>                                                                                                                                          |
| SCARD \_ E \_ WRITE \_ TOO \_ MANY<br/> 0x80100028<br/>         | Se intentó escribir más datos de los que cabría en el objeto de destino.<br/>                                                                                                                      |
| SCARD \_ F \_ COMM \_ ERROR<br/> 0x80100013<br/>              | Se ha detectado un error de comunicaciones internas.<br/>                                                                                                                                              |
| ERROR \_ INTERNO DE SCARD F \_ \_<br/> 0x80100001<br/>          | Error en una comprobación de coherencia interna.<br/>                                                                                                                                                            |
| ERROR DESCONOCIDO \_ DE SCARD F \_ \_<br/> 0x80100014<br/>           | Se ha detectado un error interno, pero se desconoce el origen.<br/>                                                                                                                                  |
| SCARD \_ F HA ESPERADO DEMASIADO \_ \_ \_ TIEMPO<br/> 0x80100007<br/>        | Ha expirado un temporizador de coherencia interno.<br/>                                                                                                                                                       |
| SCARD \_ P \_ SHUTDOWN<br/> 0x80100018<br/>                 | La operación se ha anulado para permitir que se cierre la aplicación de servidor.<br/>                                                                                                                          |
| SCARD \_ S \_ SUCCESS<br/>                                        | No se ha detectado ningún error.<br/>                                                                                                                                                                        |
| SCARD \_ W \_ CANCELLED \_ BY \_ USER<br/> 0x8010006E<br/>      | El usuario canceló la acción.<br/>                                                                                                                                                             |
| NO SE ENCONTRÓ \_ EL ELEMENTO DE CACHÉ SCARD W \_ \_ \_ \_<br/> 0x80100070<br/>  | No se encontró el elemento solicitado en la memoria caché.<br/>                                                                                                                                              |
| SCARD \_ W \_ CACHE \_ ITEM \_ STALE<br/> 0x80100071<br/>       | El elemento de caché solicitado es demasiado antiguo y se eliminó de la memoria caché.<br/>                                                                                                                              |
| SCARD \_ W \_ CACHE \_ ITEM \_ TOO \_ BIG<br/> 0x80100072<br/>    | El nuevo elemento de caché supera el tamaño máximo por elemento definido para la memoria caché.<br/>                                                                                                                      |
| TARJETA SCARD \_ W \_ NO \_ \_ AUTENTICADA<br/> 0x8010006F<br/> | No se ha presentado ningún PIN a la tarjeta inteligente.<br/>                                                                                                                                                          |
| SCARD \_ W \_ CHV \_ BLOCKED<br/> 0x8010006C<br/>             | No se puede acceder a la tarjeta porque se ha alcanzado el número máximo de intentos de entrada de PIN.<br/>                                                                                                   |
| SCARD \_ W \_ EOF<br/> 0x8010006D<br/>                      | Se ha alcanzado el final del archivo de tarjeta inteligente.<br/>                                                                                                                                                 |
| TARJETA SCARD \_ W \_ REMOVED \_<br/> 0x80100069<br/>            | Se ha quitado la tarjeta inteligente, por lo que no es posible realizar más comunicaciones.<br/>                                                                                                                       |
| SCARD \_ W \_ RESET \_ CARD<br/> 0x80100068<br/>              | Se ha restablecido la tarjeta inteligente.<br/>                                                                                                                                                                        |
| SCARD \_ W \_ INFRACCIÓN DE \_ SEGURIDAD<br/> 0x8010006A<br/>      | Se denegó el acceso debido a una infracción de seguridad.<br/>                                                                                                                                               |
| TARJETA SCARD \_ W \_ SIN \_ POTENCIA<br/> 0x80100067<br/>          | Se ha quitado la energía de la tarjeta inteligente, por lo que no es posible realizar más comunicaciones.<br/>                                                                                                       |
| TARJETA SCARD \_ W \_ NO RESPONDE \_<br/> 0x80100066<br/>       | La tarjeta inteligente no responde a un restablecimiento.<br/>                                                                                                                                                     |
| TARJETA SCARD \_ W \_ NO \_ COMPATIBLE<br/> 0x80100065<br/>        | El lector no puede comunicarse con la tarjeta debido a conflictos de configuración de cadenas atr.<br/>                                                                                                          |
| SCARD \_ W \_ WRONG \_ CHV<br/> 0x8010006B<br/>               | No se puede acceder a la tarjeta porque se presentó un PIN incorrecto.<br/>                                                                                                                                 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Códigos de error del sistema](/windows/desktop/Debug/system-error-codes)
</dt> </dl>

 

