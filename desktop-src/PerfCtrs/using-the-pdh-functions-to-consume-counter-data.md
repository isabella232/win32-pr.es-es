---
description: Las funciones de PDH se usan para recopilar datos de rendimiento.
ms.assetid: 2510480e-cfea-4f7c-af0b-6d229c150c91
title: Usar las funciones de PDH para consumir datos de contador
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 431bf160ef6ca54b4a37363d7fe6ed48bb25d953
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909706"
---
# <a name="using-the-pdh-functions-to-consume-counter-data"></a>Usar las funciones de PDH para consumir datos de contador

Utilice las funciones de PDH para recopilar datos de rendimiento. Las funciones de PDH son más fáciles de usar que las [funciones del registro](using-the-registry-functions-to-consume-counter-data.md) y se pueden usar para tener acceso a los datos de los contadores V1 y V2. PDH tiene API para recopilar datos de rendimiento actuales, guardar datos de rendimiento en archivos de registro y leer datos de archivos de registro.

> [!Note]
> No puede usar las funciones de capa de abstracción auxiliar de datos de rendimiento si está escribiendo aplicaciones de Windows OneCore. En su lugar, use [las funciones de consumidor de Perflib V2](using-the-perflib-functions-to-consume-counter-data.md).

PDH es una API de alto nivel que simplifica la recopilación de datos de contadores de rendimiento. Ayuda con el análisis de consultas, el almacenamiento en caché de metadatos, la coincidencia de instancias entre ejemplos, el cálculo de valores con formato de valores sin formato, la lectura de datos de archivos de registro y el almacenamiento de datos en archivos de registro. PDH utiliza automáticamente las [funciones del registro](using-the-registry-functions-to-consume-counter-data.md) cuando se recopilan datos de los **proveedores v1** y usa las [funciones del consumidor V2](using-the-perflib-functions-to-consume-counter-data.md) al recopilar datos de **proveedores V2**.

Para recopilar datos de rendimiento mediante las funciones de PDH, realice los pasos siguientes.

1. [Creación de una consulta](creating-a-query.md)
2. [Agregar contadores a la consulta](creating-a-query.md)
3. [Recopilar los datos de rendimiento](collecting-performance-data.md)
4. [Mostrar los datos de rendimiento](displaying-performance-data.md)
5. [Cerrar la consulta](creating-a-query.md)

Puede recopilar datos de rendimiento de orígenes en tiempo real o archivos de registro. Para obtener más información sobre cómo escribir datos de rendimiento en archivos de registro, vea [trabajar con archivos de registro](working-with-log-files.md).

## <a name="see-also"></a>Vea también

- [Recopilación de datos de rendimiento](collecting-performance-data.md)
- [Examinar contadores](browsing-counters.md)
- [Comprobar los valores devueltos de la interfaz PDH](checking-pdh-interface-return-values.md)
- [Ejemplos](examples.md)
