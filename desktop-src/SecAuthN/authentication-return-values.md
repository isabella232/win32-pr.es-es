---
description: Enumera los valores devueltos por las funciones en las API de autenticación.
ms.assetid: ea519e5c-98b0-4a01-b2cc-e5ff736a5396
title: Valores devueltos de autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2831fbce55523b3d55a649ef18fb6a622f3ec0ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082880"
---
# <a name="authentication-return-values"></a>Valores devueltos de autenticación

## <a name="network-provider-values"></a>Valores de proveedor de red

La [API del proveedor de red](network-provider-api.md) usa los siguientes valores definidos.



| Value                                                                           | Descripción                                               |
|---------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Valores devueltos de seguridad de red](network-security-return-values.md)<br/> | Valores devueltos que puede establecer un proveedor de red.<br/> |



 

## <a name="smart-card-return-values"></a>Valores devueltos de tarjeta inteligente

[Las funciones de tarjeta inteligente](authentication-functions.md) devuelven los siguientes valores devueltos. Estos valores devueltos se definen en Scarderr. h.

> [!Note]  
> Algunos valores devueltos pueden tener el mismo valor que los valores devueltos de Windows existentes que indican una condición similar. Para obtener información sobre los códigos de error que no se enumeran aquí, consulte [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

 



| Value                                                               | Descripción                                                                                                                                                                                                 |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ERROR \_ de \_ canalización interrumpida<br/> 0x00000109<br/>                | El cliente intentó realizar una operación de tarjeta inteligente en una sesión remota, como una sesión de cliente que se ejecuta en un servidor de Terminal Server, y el sistema operativo en uso no admite la redirección de tarjetas inteligentes.<br/> |
| E/ \_ s \_ defectuosa \_<br/> 0x80100029<br/>                | Error al establecer el puntero de objeto de archivo de tarjeta inteligente.<br/>                                                                                                                                 |
| PPAC \_ E \_ cancelado<br/> 0x80100002<br/>                | Una solicitud [**SCardCancel**](/windows/desktop/api/Winscard/nf-winscard-scardcancel) canceló la acción.<br/>                                                                                                                        |
| no se \_ pudo \_ \_ eliminar la PPAC<br/> 0x8010000E<br/>            | El sistema no pudo eliminar el medio de la manera solicitada.<br/>                                                                                                                               |
| \_ \_ tarjeta E \_ no compatible<br/> 0x8010001C<br/>        | La tarjeta inteligente no cumple los requisitos mínimos de soporte técnico.<br/>                                                                                                                                   |
| certificado de \_ E \_ \_ no disponible<br/> 0x8010002D<br/> | No se pudo obtener el certificado solicitado.<br/>                                                                                                                                                 |
| se \_ \_ \_ han perdido datos de comunicaciones de E/s \_<br/> 0x8010002F<br/>         | Se ha detectado un error de comunicación con la tarjeta inteligente. <br/>                                                                                                                                   |
| \_ \_ \_ no se encontró el directorio \_ SCard E<br/> 0x80100023<br/>          | El directorio especificado no existe en la tarjeta inteligente.<br/>                                                                                                                                        |
| lector de \_ \_ duplicados E duplicados \_<br/> 0x8010001B<br/>        | El controlador de [*lector*](/windows/desktop/SecGloss/r-gly) no produjo un nombre de lector único.<br/>                                                                            |
| archivo de \_ PPAC \_ E \_ no \_ encontrado<br/> 0x80100024<br/>         | El archivo especificado no existe en la tarjeta inteligente.<br/>                                                                                                                                             |
| \_ \_ \_ CREATEORDER ICC<br/> 0x80100021<br/>         | No se admite el orden solicitado de creación de objetos.<br/>                                                                                                                                         |
| instalación de \_ \_ ICC E ICC \_<br/> 0x80100020<br/>        | No se puede encontrar ningún proveedor principal para la tarjeta inteligente.<br/>                                                                                                                                             |
| \_ \_ búfer insuficiente en \_ PPAC<br/> 0x80100008<br/>     | El búfer de datos para los datos devueltos es demasiado pequeño para los datos devueltos.<br/>                                                                                                                            |
| E/ \_ s \_ no válida ( \_ ATR)<br/> 0x80100015<br/>             | Una [*cadena ATR*](/windows/desktop/SecGloss/a-gly) obtenida del registro no es una cadena ATR válida.<br/>                                                        |
| \_ \_ invalid E CHV no válidos \_<br/> 0x8010002A<br/>             | El PIN proporcionado no es correcto.<br/>                                                                                                                                                                   |
| \_ \_ identificador no válido de \_ PPAC<br/> 0x80100003<br/>          | El identificador proporcionado no era válido.<br/>                                                                                                                                                               |
| parámetro de PPACd \_ E \_ no válido \_<br/> 0x80100004<br/>       | Uno o varios de los parámetros proporcionados no se pudieron interpretar correctamente.<br/>                                                                                                                        |
| \_ \_ destino no válido de \_ PPAC<br/> 0x80100005<br/>          | Falta la información de inicio del registro o no es válida.<br/>                                                                                                                                            |
| valor de PPAC \_ E \_ no válido \_<br/> 0x80100011<br/>           | Uno o varios de los valores de parámetro proporcionados no se pudieron interpretar correctamente.<br/>                                                                                                                  |
| NO se ha podido \_ \_ \_ obtener acceso<br/> 0x80100027<br/>               | Se denegó el acceso al archivo.<br/>                                                                                                                                                                    |
| número de \_ \_ \_ directorios<br/> 0x80100025<br/>                  | La ruta de acceso proporcionada no representa un directorio de tarjeta inteligente.<br/>                                                                                                                                     |
| \_ \_ no hay \_ archivo<br/> 0x80100026<br/>                 | La ruta de acceso proporcionada no representa un archivo de tarjeta inteligente.<br/>                                                                                                                                          |
| NO se ha podido incluir \_ \_ un \_ contenedor de claves \_<br/> 0x80100030<br/>       | El contenedor de claves solicitado no existe en la tarjeta inteligente.<br/>                                                                                                                                    |
| \_ \_ no hay \_ memoria<br/> 0x80100006<br/>               | No hay suficiente memoria disponible para completar este comando.<br/>                                                                                                                                            |
| \_ \_ \_ memoria caché de PIN inexistente \_<br/> 0x80100033<br/>           | No se puede almacenar en caché el PIN de la tarjeta inteligente.<br/> **Windows server 2008, Windows Vista, Windows server 2003 y Windows XP:** Este código de error no está disponible.<br/> <br/>                        |
| PPAC \_ E \_ no hay \_ lectores \_ disponibles<br/> 0x8010002E<br/>   | No hay ningún lector de tarjeta inteligente disponible.<br/>                                                                                                                                                               |
| \_ \_ no hay ningún \_ servicio<br/> 0x8010001D<br/>              | No se está ejecutando el [*Administrador de recursos*](/windows/desktop/SecGloss/r-gly) de tarjeta inteligente.<br/>                                                                |
| \_ \_ tarjeta inteligente E no \_<br/> 0x8010000C<br/>            | La operación requiere una tarjeta inteligente, pero actualmente no hay ninguna tarjeta inteligente en el dispositivo.<br/>                                                                                                               |
| \_ \_ no existe \_ tal \_ certificado<br/> 0x8010002C<br/>    | El certificado solicitado no existe.<br/>                                                                                                                                                        |
| PPAC \_ E \_ no \_ listo<br/> 0x80100010<br/>               | El lector o la tarjeta no están listos para aceptar comandos.<br/>                                                                                                                                              |
| PPAC \_ E \_ sin \_ transacciones<br/> 0x80100016<br/>          | Se ha intentado finalizar una transacción inexistente.<br/>                                                                                                                                            |
| PCI de \_ PPAC \_ \_ es demasiado \_ pequeño<br/> 0x80100019<br/>          | El búfer de recepción PCI era demasiado pequeño.<br/>                                                                                                                                                            |
| \_ \_ memoria caché de PIN de PPAC \_ \_ expirada<br/> 0x80100032<br/>      | La memoria caché de PIN de tarjeta inteligente ha expirado.<br/> **Windows server 2008, Windows Vista, Windows server 2003 y Windows XP:** Este código de error no está disponible.<br/> <br/>                       |
| \_ \_ no coinciden el proto de E/s \_<br/> 0x8010000F<br/>          | Los protocolos solicitados son incompatibles con el protocolo que se usa actualmente con la tarjeta.<br/>                                                                                                       |
| tarjeta de \_ \_ solo lectura y de \_ solo lectura \_<br/> 0x80100034<br/>         | La tarjeta inteligente es de solo lectura y no se puede escribir en ella.<br/> **Windows server 2008, Windows Vista, Windows server 2003 y Windows XP:** Este código de error no está disponible.<br/> <br/>       |
| lector de \_ PPAC \_ E \_ no disponible<br/> 0x80100017<br/>      | El lector especificado no está disponible actualmente para su uso.<br/>                                                                                                                                         |
| lector de \_ PPAC \_ E \_ no compatible<br/> 0x8010001A<br/>      | El controlador de lector no cumple los requisitos mínimos de soporte técnico.<br/>                                                                                                                                |
| el \_ servidor E \_ está \_ \_ disponible demasiado ocupado<br/> 0x80100031<br/>        | El administrador de recursos de tarjeta inteligente está demasiado ocupado para completar esta operación.<br/>                                                                                                                          |
| se \_ \_ detuvo el servicio de E/s \_<br/> 0x8010001E<br/>         | Se ha cerrado el administrador de recursos de tarjeta inteligente.<br/>                                                                                                                                                   |
| infracción \_ de \_ uso compartido de PPAC \_<br/> 0x8010000B<br/>       | No se puede tener acceso a la tarjeta inteligente debido a otras conexiones pendientes.<br/>                                                                                                                      |
| \_ \_ sistema integrado E \_ cancelado<br/> 0x80100012<br/>        | El sistema canceló la acción, presumiblemente cerrarla o cerrarla.<br/>                                                                                                                       |
| tiempo de espera de PPAC \_ E \_<br/> 0x8010000A<br/>                  | El valor de tiempo de espera especificado por el usuario ha expirado.<br/>                                                                                                                                                   |
| PPAC \_ E \_ inesperado<br/> 0x8010001F<br/>               | Error de tarjeta inesperado.<br/>                                                                                                                                                           |
| \_ \_ tarjeta desconocida E desconocida \_<br/> 0x8010000D<br/>            | No se reconoce el nombre de la tarjeta inteligente especificado.<br/>                                                                                                                                                 |
| \_ \_ lector desconocido E desconocido \_<br/> 0x80100009<br/>          | No se reconoce el nombre de lector especificado.<br/>                                                                                                                                                     |
| MNG de \_ \_ res desconocida E desconocido \_ \_<br/> 0x8010002B<br/>        | Se devolvió un código de error no reconocido.<br/>                                                                                                                                                         |
| característica de PPAC \_ E \_ no compatible \_<br/> 0x80100022<br/>     | Esta tarjeta inteligente no es compatible con la característica solicitada.<br/>                                                                                                                                          |
| \_E \_ Escriba \_ demasiadas \_<br/> 0x80100028<br/>         | Se intentó escribir más datos de los que caben en el objeto de destino.<br/>                                                                                                                      |
| ERROR de \_ comunicación de F \_ \_<br/> 0x80100013<br/>              | Se ha detectado un error interno de comunicaciones.<br/>                                                                                                                                              |
| \_ \_ error interno de v \_<br/> 0x80100001<br/>          | Error de comprobación de coherencia interna.<br/>                                                                                                                                                            |
| \_error desconocido de F de PPAC \_ \_<br/> 0x80100014<br/>           | Se detectó un error interno, pero se desconoce el origen.<br/>                                                                                                                                  |
| se ha \_ \_ esperado un \_ \_ tiempo demasiado largo<br/> 0x80100007<br/>        | Expiró un temporizador de coherencia interno.<br/>                                                                                                                                                       |
| apagado de \_ P \_<br/> 0x80100018<br/>                 | La operación se ha anulado para permitir que la aplicación de servidor se cierre.<br/>                                                                                                                          |
| operación de \_ \_ corrección correcta<br/>                                        | No se ha detectado ningún error.<br/>                                                                                                                                                                        |
| PPAC \_ W \_ cancelado \_ por el \_ usuario<br/> 0x8010006E<br/>      | El usuario canceló la acción.<br/>                                                                                                                                                             |
| \_ \_ \_ \_ no \_ se encontró el elemento de caché de PPAC<br/> 0x80100070<br/>  | No se encontró el elemento solicitado en la memoria caché.<br/>                                                                                                                                              |
| \_ \_ elemento almacenado en caché \_ \_ obsoleto<br/> 0x80100071<br/>       | El elemento de caché solicitado es demasiado antiguo y se eliminó de la memoria caché.<br/>                                                                                                                              |
| el elemento de caché de PPAC \_ \_ \_ \_ es demasiado \_ grande<br/> 0x80100072<br/>    | El nuevo elemento de caché supera el tamaño máximo por elemento definido para la memoria caché.<br/>                                                                                                                      |
| tarjeta de \_ PPAC \_ W \_ no \_ autenticada<br/> 0x8010006F<br/> | No se presentó ningún PIN a la tarjeta inteligente.<br/>                                                                                                                                                          |
| no se \_ ha \_ bloqueado el CHV \_<br/> 0x8010006C<br/>             | No se puede tener acceso a la tarjeta porque se ha alcanzado el número máximo de intentos de entrada de PIN.<br/>                                                                                                   |
| EOF en \_ t \_<br/> 0x8010006D<br/>                      | Se ha alcanzado el final del archivo de tarjeta inteligente.<br/>                                                                                                                                                 |
| tarjeta con la que se ha \_ \_ quitado la \_ tarjeta<br/> 0x80100069<br/>            | La tarjeta inteligente se ha quitado, por lo que no es posible realizar más comunicaciones.<br/>                                                                                                                       |
| tarjeta de \_ \_ restablecimiento W \_<br/> 0x80100068<br/>              | Se restableció la tarjeta inteligente.<br/>                                                                                                                                                                        |
| infracción de seguridad de PPAC \_ W \_ \_<br/> 0x8010006A<br/>      | Se denegó el acceso debido a una infracción de seguridad.<br/>                                                                                                                                               |
| tarjeta no \_ \_ alimentada sin alimentación \_<br/> 0x80100067<br/>          | La alimentación se ha quitado de la tarjeta inteligente para que no sea posible la comunicación adicional.<br/>                                                                                                       |
| tarjeta no \_ \_ responde \_<br/> 0x80100066<br/>       | La tarjeta inteligente no responde a un restablecimiento.<br/>                                                                                                                                                     |
| \_ \_ tarjeta no admitida \_<br/> 0x80100065<br/>        | El lector no puede comunicarse con la tarjeta debido a conflictos de configuración de cadena ATR.<br/>                                                                                                          |
| no se ha indicado un \_ \_ \_ CHV erróneo<br/> 0x8010006B<br/>               | No se puede obtener acceso a la tarjeta porque se presentó el PIN equivocado.<br/>                                                                                                                                 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Códigos de error del sistema](/windows/desktop/Debug/system-error-codes)
</dt> </dl>

 

