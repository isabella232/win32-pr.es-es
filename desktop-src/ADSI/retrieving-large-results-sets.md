---
title: Recuperar grandes conjuntos de resultados
description: Cuando existe la posibilidad de que el conjunto de resultados que se devolverá contenga más de 1000 elementos, debe usar una búsqueda paginada.
ms.assetid: 1439d6b8-50dd-4d37-bcc9-dd0f63af865f
ms.tgt_platform: multiple
keywords:
- Recuperar adsi de conjuntos de resultados grandes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d5a8f920da20de70538a57674b00de33ac6df3a6f4b12e6027134557fd9ee28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119391805"
---
# <a name="retrieving-large-results-sets"></a>Recuperar grandes conjuntos de resultados

Cuando existe la posibilidad de que el conjunto de resultados que se devolverá contenga más de 1000 elementos, debe usar una búsqueda paginada. Las búsquedas Active Directory realizadas sin paginación se limitan a devolver un máximo de los primeros 1000 registros. Con una búsqueda paginada, el conjunto de resultados se presenta como páginas individuales, cada una de las que contiene un número predeterminado de entradas de resultado. Con este tipo de búsqueda, se devuelven nuevas páginas de entradas de resultado hasta que se alcanza el final del conjunto de resultados.

De forma predeterminada, el servidor que responde a una solicitud de consulta calcula completamente un conjunto de resultados antes de devolver datos. En un conjunto de resultados grande, esto requiere memoria del servidor a medida que se adquiere el conjunto de resultados y ancho de banda de red cuando se devuelve el resultado grande. Establecer un tamaño de página permite al servidor enviar los datos en páginas a medida que se están construyendo las páginas. A continuación, el cliente almacena en caché estos datos y proporciona un cursor al código de nivel de aplicación. La paginación se establece mediante la definición del número de filas que calcula el servidor antes de que los datos se devuelvan a través de la red al cliente.

La búsqueda paginada ofrece ventajas tanto para el cliente como para el servidor. Por ejemplo, el cliente puede tener más capacidad de respuesta para presentar los resultados a los usuarios finales. Esto es especialmente relevante para las herramientas gráficas de interfaz de usuario que pueden mostrar datos mientras otro subproceso recibe simultáneamente más datos del servidor.

Al configurar la consulta, si especifica un criterio de ordenación para el conjunto de resultados, el servidor debe calcular completamente el conjunto de resultados antes de devolver los datos al cliente, lo que afecta al tiempo de respuesta de la consulta.

En el lado servidor, la búsqueda paginada hace que la operación sea escalable. Por ejemplo, si cien clientes emiten solicitudes de búsqueda simultáneamente y, de media, a cada cliente se le devuelven 200 objetos, si no se especifica el tamaño de página, el servidor debe tener suficiente memoria para contener el conjunto de resultados completo de 20 000 entradas. Como alternativa, si cada cliente especificase un tamaño de página de diez objetos, los requisitos de memoria del servidor se reducirían en un factor de 20.

> [!Note]  
> No todos los servicios de directorio admiten búsquedas paginadas. Active Directory implementa la arquitectura de tamaño de página.

 

Muchos servidores de directorio especifican un límite administrativo para el número máximo de objetos que pueden devolver si un cliente no especifica el tamaño de página. Cuando se alcanza el límite administrativo, ADSI genera el **error ERROR \_ DS ADMIN LIMIT \_ \_ \_ EXCEEDED** Win32.

En el lado cliente, una búsqueda paginada permite a un cliente detener la operación mientras todavía está en curso. Por el contrario, en una búsqueda no paginada, el cliente se bloquea hasta que se devuelven completamente los datos o se produce un error. Esto podría afectar al rendimiento de la red si el conjunto de resultados resulta ser mayor y tarda más de lo esperado.

En nombre del cliente, ADSI controla el tamaño de página de forma transparente. El cliente no tiene que contar el número de objetos en curso. ADSI encapsula la interacción del servidor para el cliente. Desde la perspectiva del cliente, la búsqueda devuelve un conjunto de resultados completo.

Para obtener más información sobre el uso de la opción de tiempo de espera de búsqueda con una interfaz de búsqueda específica, vea:

-   [Paginación con IDirectorySearch](paging-with-idirectorysearch.md)
-   [Búsqueda con objetos ActiveX datos](searching-with-activex-data-objects-ado.md)
-   [Búsqueda con OLE DB](searching-with-ole-db.md)

Una búsqueda paginada es transparente para la aplicación porque ADSI continúa recuperando automáticamente páginas de resultados adicionales hasta que alcanza el final del conjunto de resultados o el final del límite de tiempo establecido. Cuando se usa una búsqueda paginada, el límite de tamaño no invalida el tamaño de página. El límite de tamaño solo se puede usar cuando se recupera un conjunto de resultados que contiene menos de 1000 entradas.

 

 




