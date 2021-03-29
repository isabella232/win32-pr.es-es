---
title: Registro de IIS
description: El registro de IIS es un tipo de registro del lado servidor que se puede habilitar en un grupo de direcciones URL.
ms.assetid: 2adfee73-090a-4bc1-827e-4b0e8075e2b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79d438d0926be2579fa526cc126c7f635a6eecd5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665715"
---
# <a name="iis-logging"></a>Registro de IIS

El registro de IIS es un tipo de registro del lado servidor que se puede habilitar en un grupo de direcciones URL. El formato de archivo de registro de IIS es un formato basado en texto ASCII fijo que no se puede personalizar. El archivo de registro de IIS contiene los aciertos de caché del modo kernel de la API del servidor HTTP. Este tipo de registro solo se puede habilitar en un grupo de direcciones URL; no se puede usar en la sesión de servidor.

El formato de archivo de registro de IIS registra los datos siguientes. Los datos de la tabla están en el orden de aparición en el archivo de registro.



| Campo                | Descripción                                                                                                                                                                       |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dirección IP de cliente    | Dirección IP del cliente que realizó la solicitud.                                                                                                                               |
| Nombre de usuario            | Nombre del usuario autenticado que tuvo acceso al servidor. Los usuarios anónimos se indican con un guion. El procedimiento recomendado es que la aplicación siempre proporcione el nombre de usuario. |
| Fecha                 | Fecha en la que se produjo la actividad.                                                                                                                                          |
| Hora                 | La hora local en la que se produjo la actividad.                                                                                                                                    |
| Servicio e instancia | El nombre del servicio de Internet y el número de instancia que se estaba ejecutando en el cliente.                                                                                                     |
| Nombre de servidor          | Nombre del servidor en el que se generó la entrada del archivo de registro.                                                                                                                 |
| Dirección IP del servidor    | Dirección IP del servidor en el que se generó la entrada del archivo de registro.                                                                                                           |
| Tiempo empleado           | El período de tiempo que tardó la acción, en milisegundos.                                                                                                                         |
| Bytes de cliente enviados    | Número de bytes enviados por el cliente.                                                                                                                                           |
| Bytes de servidor enviados    | Número de bytes enviados por el servidor.                                                                                                                                           |
| Código de estado del servicio  | Un valor de 200 indica que la solicitud se completó correctamente.                                                                                                             |
| Código de estado de Windows  | Un valor de 0 (cero) indica que la solicitud se completó correctamente.                                                                                                        |
| Tipo de solicitud         | El verbo de la solicitud.                                                                                                                                                                 |
| Destino de la operación  | El destino del verbo, por ejemplo, Default.htm.                                                                                                                                 |
| Parámetros           | Los parámetros que se pasan a un scripts.                                                                                                                                        |



 

No todos los campos contendrán información. En el caso de los campos para los que no hay información, aparece un guion (-) como marcador de posición. Si un campo contiene un carácter no imprimible, la API del servidor HTTP lo reemplaza con un signo más (+) para conservar el formato del archivo de registro. Esto suele ocurrir con ataques de virus, cuando, por ejemplo, un usuario malintencionado envía retornos de carro y saltos de línea que, si no se reemplazan por el signo más (+), interrumpiría el formato del archivo de registro. Los campos se separan mediante comas, lo que facilita la lectura del formato que los demás formatos ASCII, que usan espacios para los separadores. La hora se registra como hora local. El tiempo necesario se registra en milisegundos. Para obtener más información acerca del campo tiempo empleado, vea el tema [registro W3C](w3c-logging.md) .

En el ejemplo siguiente se muestra una entrada de archivo de registro común de NCSA.

``` syntax
192.168.114.201, -, 03/20/05, 7:55:20, W3SVC2, SERVER, 
172.21.13.45, 4502, 163, 3223, 200, 0, GET, /DeptLogo.gif, -,
```

 

 




