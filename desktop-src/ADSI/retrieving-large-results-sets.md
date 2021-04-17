---
title: Recuperar conjuntos de resultados grandes
description: Si existe la posibilidad de que el conjunto de resultados que se devuelva contenga más de 1000 elementos, debe usar una búsqueda paginada.
ms.assetid: 1439d6b8-50dd-4d37-bcc9-dd0f63af865f
ms.tgt_platform: multiple
keywords:
- Recuperar conjuntos de resultados de gran tamaño ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78f8902d25010690953cfae8a03ff9e500b4ebda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656154"
---
# <a name="retrieving-large-results-sets"></a>Recuperar conjuntos de resultados grandes

Si existe la posibilidad de que el conjunto de resultados que se devuelva contenga más de 1000 elementos, debe usar una búsqueda paginada. Las búsquedas de Active Directory realizadas sin paginación se limitan a devolver un máximo de los primeros 1000 registros. Con una búsqueda paginada, el conjunto de resultados se presenta como páginas individuales, cada una de las cuales contiene un número predeterminado de entradas de resultados. Con este tipo de búsqueda, se devuelven nuevas páginas de entradas de resultados hasta que se alcanza el final del conjunto de resultados.

De forma predeterminada, el servidor que responde a una solicitud de consulta calcula completamente un conjunto de resultados antes de devolver los datos. En un conjunto de resultados grande, esto requiere la memoria del servidor cuando se adquiere el conjunto de resultados y el ancho de banda de red cuando se devuelve el resultado grande. Establecer un tamaño de página permite que el servidor envíe los datos en las páginas a medida que se compilan las páginas. Después, el cliente almacena en caché estos datos y proporciona un cursor al código de nivel de aplicación. La paginación se establece definiendo cuántas filas calcula el servidor antes de que los datos se devuelvan a través de la red al cliente.

La búsqueda paginada ofrece ventajas tanto para el cliente como para el servidor. Por ejemplo, el cliente puede tener mayor capacidad de respuesta en la presentación de los resultados a los usuarios finales. Esto es especialmente importante para las herramientas de interfaz gráfica de usuario que pueden mostrar datos mientras otro subproceso recibe simultáneamente más datos del servidor.

Al configurar la consulta, si especifica un criterio de ordenación para el conjunto de resultados, el servidor debe calcular por completo el conjunto de resultados antes de devolver los datos al cliente, lo que afecta al tiempo de respuesta de la consulta.

En el lado del servidor, la búsqueda paginada hace que la operación sea escalable. Por ejemplo, si los clientes 100 emiten solicitudes de búsqueda simultáneamente y, en el promedio, cada cliente devuelve 200 objetos, si no se especifica el tamaño de página, el servidor debe tener suficiente memoria para contener el conjunto de resultados completo de 20.000 entradas. Como alternativa, si cada cliente especifica un tamaño de página de diez objetos, los requisitos de memoria en el servidor se reducirían en un factor de 20.

> [!Note]  
> No todos los servicios de directorio admiten búsquedas paginadas. Active Directory implementa la arquitectura de tamaño de página.

 

Muchos servidores de directorio especifican un límite administrativo para el número máximo de objetos que pueden devolver si un cliente no especifica el tamaño de página. Cuando se alcanza el límite administrativo, ADSI genera el error Error de Win32 de **\_ límite de \_ Administración \_ \_ de DS** .

En el lado del cliente, una búsqueda paginada permite a un cliente detener la operación mientras aún está en curso. Por el contrario, en una búsqueda no paginada, el cliente se bloquea hasta que se devuelven los datos por completo, o se produce un error. Esto podría afectar al rendimiento de la red si el conjunto de resultados resulta ser mayor y tarda más tiempo del esperado.

En nombre del cliente, ADSI controla el tamaño de página de forma transparente. El cliente no tiene que contar el número de objetos en curso. ADSI encapsula la interacción del servidor para el cliente. Desde la perspectiva del cliente, la búsqueda devuelve un conjunto de resultados completo.

Para obtener más información acerca del uso de la opción de tiempo de espera de búsqueda con una interfaz de búsqueda específica, vea:

-   [Paginación con IDirectorySearch](paging-with-idirectorysearch.md)
-   [Buscar con Objetos de datos ActiveX](searching-with-activex-data-objects-ado.md)
-   [Buscar con OLE DB](searching-with-ole-db.md)

Una búsqueda paginada es transparente para la aplicación porque ADSI continúa recuperando automáticamente páginas de resultados adicionales hasta que llega al final del conjunto de resultados o al final del límite de tiempo establecido. Cuando se usa una búsqueda paginada, el límite de tamaño no invalida el tamaño de página. El límite de tamaño solo se puede usar cuando se recupera un conjunto de resultados que contiene menos de 1000 entradas.

 

 




