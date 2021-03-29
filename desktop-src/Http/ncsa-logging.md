---
title: Registro NCSA
description: El registro extendido NCSA es un tipo de registro del lado servidor que se puede habilitar en un grupo de direcciones URL.
ms.assetid: 14a2492a-3bcf-46f3-a3a5-1ea578516865
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f04db62d5d561fb227f7a46a33c2aefcacd943b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779489"
---
# <a name="ncsa-logging"></a>Registro NCSA

El registro extendido NCSA es un tipo de registro del lado servidor que se puede habilitar en un grupo de direcciones URL. El formato de archivo de registro común NCSA es un formato basado en texto ASCII fijo que no se puede personalizar. El archivo de registro NCSA contiene los aciertos de caché del modo kernel de la API del servidor HTTP. Este tipo de registro solo se puede habilitar en un grupo de direcciones URL; no se puede usar en la sesión de servidor.

El formato de archivo de registro común NCSA registra los datos siguientes. Los datos de la tabla están en el orden de aparición en el archivo de registro.



| Campo                                            | Descripción                                                                                                                                                                       |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dirección de host remoto                              | Dirección IP del cliente que realizó la solicitud.                                                                                                                               |
| Nombre de registro remoto                                  | No se utiliza. Este valor siempre es un guion.                                                                                                                                          |
| Nombre de usuario                                        | Nombre del usuario autenticado que tuvo acceso al servidor. Los usuarios anónimos se indican con un guion. El procedimiento recomendado es que la aplicación siempre proporcione el nombre de usuario. |
| Fecha, hora y desplazamiento de la hora del meridiano de Greenwich (GMT) | Fecha y hora locales en las que se produjo la actividad. También se indica el desplazamiento de la hora del meridiano de Greenwich.                                                                    |
| Versión de solicitud y protocolo                     | La versión del protocolo HTTP que usó el cliente.                                                                                                                                   |
| Código de estado del servicio                              | El código de estado HTTP. (Un valor de 200 indica que la solicitud se completó correctamente).                                                                                         |
| Bytes enviados                                       | Número de bytes enviados por el servidor.                                                                                                                                           |



 

No todos los campos contendrán información. En el caso de los campos para los que no hay información, aparece un guion (-) como marcador de posición. Si un campo contiene un carácter no imprimible, la API del servidor HTTP lo reemplaza con un signo más (+) para conservar el formato del archivo de registro. Esto suele ocurrir con ataques de virus, cuando, por ejemplo, un usuario malintencionado envía retornos de carro y saltos de línea que, si no se reemplazan por el signo más (+), interrumpiría el formato del archivo de registro. Los campos están separados por espacios y la hora se registra como hora local con el desplazamiento GMT.

En el ejemplo siguiente se muestra una entrada de archivo de registro común de NCSA, tal como se ve en un editor de texto.

``` syntax
172.21.13.45 - Microsoft\JohnDoe [07/Apr/2004:17:39:04 -0800] 
"GET /scripts/iisadmin/ism.dll?http/serv HTTP/1.0" 200 3401
```

La dirección IP del cliente es 172.21.13.45 y el nombre de usuario es Microsoft de Microsoft \\ . El registro se registró el 7 de abril de 2005 a la hora local 17:39:04 con un desplazamiento de Greenwich de 8 horas. El verbo de solicitud y la versión del protocolo eran "GET/scripts/iisadmin/ism.dll? http/serv HTTP/1.0". Los códigos de Estado eran 200 correctos y el número de bytes enviados por el cliente era 3401.

 

 




