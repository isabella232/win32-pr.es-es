---
title: Registro de IIS
description: El registro de IIS es un tipo de registro del lado servidor que se puede habilitar en un grupo de direcciones URL.
ms.assetid: 2adfee73-090a-4bc1-827e-4b0e8075e2b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecd92582e048a3b1a27d88f50f33c368345c72a836b72de9f2abb777bf5e9c59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102105"
---
# <a name="iis-logging"></a>Registro de IIS

El registro de IIS es un tipo de registro del lado servidor que se puede habilitar en un grupo de direcciones URL. El formato del archivo de registro de IIS es un formato fijo basado en texto ASCII que no se puede personalizar. El archivo de registro de IIS contiene los aciertos de caché en modo kernel de la API del servidor HTTP. Este tipo de registro solo se puede habilitar en un grupo de direcciones URL; no se puede usar en la sesión del servidor.

El formato de archivo de registro de IIS registra los datos siguientes. Los datos de la tabla están en el orden de aparición en el archivo de registro.



| Campo                | Descripción                                                                                                                                                                       |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dirección IP de cliente    | Dirección IP del cliente que realizó la solicitud.                                                                                                                               |
| Nombre de usuario            | Nombre del usuario autenticado que ha accedido al servidor. Los usuarios anónimos se indican con un guion. El procedimiento recomendado es que la aplicación proporcione siempre el nombre de usuario. |
| Date                 | Fecha en la que se produjo la actividad.                                                                                                                                          |
| Time                 | Hora local a la que se produjo la actividad.                                                                                                                                    |
| Servicio e instancia | El nombre del servicio de Internet y el número de instancia que se estaba ejecutando en el cliente.                                                                                                     |
| Nombre de servidor          | Nombre del servidor en el que se generó la entrada del archivo de registro.                                                                                                                 |
| Dirección IP del servidor    | Dirección IP del servidor en el que se generó la entrada del archivo de registro.                                                                                                           |
| Tiempo empleado           | El período de tiempo que tardó la acción, en milisegundos.                                                                                                                         |
| Bytes de cliente enviados    | Número de bytes enviados por el cliente.                                                                                                                                           |
| Bytes de servidor enviados    | Número de bytes enviados por el servidor.                                                                                                                                           |
| Código de estado del servicio  | Un valor de 200 indica que la solicitud se ha realizado correctamente.                                                                                                             |
| Windows de estado  | Un valor de 0 (cero) indica que la solicitud se ha completado correctamente.                                                                                                        |
| Tipo de solicitud         | Verbo de solicitud.                                                                                                                                                                 |
| Destino de la operación  | El destino del verbo, por ejemplo, Default.htm.                                                                                                                                 |
| Parámetros           | Parámetros que se pasan a un scrip.                                                                                                                                        |



 

No todos los campos contendrán información. Para los campos para los que no hay información, aparece un guion (-) como marcador de posición. Si un campo contiene un carácter no imprimible, la API del servidor HTTP lo reemplaza por un signo más (+) para conservar el formato del archivo de registro. Esto suele ocurrir con ataques de virus, cuando, por ejemplo, un usuario malintencionado envía retornos de carro y avances de línea que, si no se reemplazan por el signo más (+), interrumpirían el formato del archivo de registro. Los campos están separados por comas, lo que facilita la lectura del formato que los demás formatos ASCII, que usan espacios para los separadores. La hora se registra como hora local. El tiempo que se toma se registra en milisegundos. Para obtener más información sobre el campo de tiempo que se ha realizado, vea el tema [Registro de W3C.](w3c-logging.md)

En el ejemplo siguiente se muestra una entrada de archivo de registro común ncSA.

``` syntax
192.168.114.201, -, 03/20/05, 7:55:20, W3SVC2, SERVER, 
172.21.13.45, 4502, 163, 3223, 200, 0, GET, /DeptLogo.gif, -,
```

 

 




