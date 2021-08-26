---
title: Registro de NCSA
description: El registro extendido de NCSA es un tipo de registro del lado servidor que se puede habilitar en un grupo de direcciones URL.
ms.assetid: 14a2492a-3bcf-46f3-a3a5-1ea578516865
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9a5b9ef608da18264f4534c7e50e9672794a21bc61c91741feeb9e814c7afc8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078315"
---
# <a name="ncsa-logging"></a>Registro de NCSA

El registro extendido de NCSA es un tipo de registro del lado servidor que se puede habilitar en un grupo de direcciones URL. El formato de archivo de registro común ncSA es un formato fijo basado en texto ASCII que no se puede personalizar. El archivo de registro NCSA contiene los aciertos de caché en modo kernel de la API del servidor HTTP. Este tipo de registro solo se puede habilitar en un grupo de direcciones URL; no se puede usar en la sesión del servidor.

El formato de archivo de registro común de NCSA registra los datos siguientes. Los datos de la tabla están en el orden de aparición en el archivo de registro.



| Campo                                            | Descripción                                                                                                                                                                       |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dirección de host remoto                              | Dirección IP del cliente que realizó la solicitud.                                                                                                                               |
| Nombre del registro remoto                                  | No se usa. Este valor siempre es un guión.                                                                                                                                          |
| Nombre de usuario                                        | Nombre del usuario autenticado que ha accedido al servidor. Los usuarios anónimos se indican con un guion. El procedimiento recomendado es que la aplicación proporcione siempre el nombre de usuario. |
| Desplazamiento de fecha, hora y hora media de Greenwich (GMT) | Fecha y hora locales en las que se produjo la actividad. También se indica el desplazamiento de la hora media de Greenwich.                                                                    |
| Versión de solicitud y protocolo                     | Versión del protocolo HTTP que usó el cliente.                                                                                                                                   |
| Código de estado del servicio                              | El código de estado HTTP. (Un valor de 200 indica que la solicitud se completó correctamente).                                                                                         |
| Bytes enviados                                       | Número de bytes enviados por el servidor.                                                                                                                                           |



 

No todos los campos contendrán información. Para los campos para los que no hay información, aparece un guion (-) como marcador de posición. Si un campo contiene un carácter no imprimible, la API del servidor HTTP lo reemplaza por un signo más (+) para conservar el formato del archivo de registro. Esto suele ocurrir con ataques de virus, cuando, por ejemplo, un usuario malintencionado envía retornos de carro y avances de línea que, si no se reemplazan por el signo más (+), interrumpirían el formato del archivo de registro. Los campos están separados por espacios y la hora se registra como hora local con el desplazamiento GMT.

En el ejemplo siguiente se muestra una entrada de archivo de registro común ncSA, como se ve en un editor de texto.

``` syntax
172.21.13.45 - Microsoft\JohnDoe [07/Apr/2004:17:39:04 -0800] 
"GET /scripts/iisadmin/ism.dll?http/serv HTTP/1.0" 200 3401
```

La dirección IP del cliente es 172.21.13.45 y el nombre de usuario es Microsoft \\ JohnDoe. El registro se registró el 7 de abril de 2005 a las 17:39:04 hora local con un desplazamiento de Greenwich de 8 horas. El verbo de solicitud y la versión del protocolo eran "GET /scripts/iisadmin/ism.dll?http/serv HTTP/1.0". Los códigos de estado son 200 correctos y el número de bytes enviados por el cliente es 3401.

 

 




