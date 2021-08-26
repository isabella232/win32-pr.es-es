---
description: Las funciones PDH se usan para recopilar datos de rendimiento.
ms.assetid: 2510480e-cfea-4f7c-af0b-6d229c150c91
title: Uso de las funciones PDH para consumir datos de contador
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 6c506e3c7a73a94a6bc3c282920e17504e28dedb42e0e3bee8a6f05a1e77ebbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033195"
---
# <a name="using-the-pdh-functions-to-consume-counter-data"></a>Uso de las funciones PDH para consumir datos de contador

Use las funciones PDH para recopilar datos de rendimiento. Las funciones PDH son más [](using-the-registry-functions-to-consume-counter-data.md) fáciles de usar que las funciones del Registro y se pueden usar para acceder a los datos de contadores de proveedores V1 y V2. PDH tiene API para recopilar datos de rendimiento actuales, guardar datos de rendimiento en archivos de registro y leer datos de archivos de registro.

> [!Note]
> No puede usar las funciones de capa de abstracción del asistente de datos de rendimiento si está escribiendo Windows OneCore aplicaciones. En su lugar, use [las funciones de consumidor de PerfLib V2](using-the-perflib-functions-to-consume-counter-data.md).

PDH es una API de alto nivel que simplifica la recopilación de datos de contadores de rendimiento. Ayuda con el análisis de consultas, el almacenamiento en caché de metadatos, la coincidencia de instancias entre ejemplos, la computación de valores con formato a partir de valores sin procesar, la lectura de datos de archivos de registro y el guardado de datos en archivos de registro. PDH usa automáticamente [](using-the-registry-functions-to-consume-counter-data.md) las funciones del Registro al recopilar datos de proveedores **V1** y usa las funciones de consumidor [V2](using-the-perflib-functions-to-consume-counter-data.md) al recopilar datos de proveedores **V2.**

Para recopilar datos de rendimiento mediante las funciones PDH, realice los pasos siguientes.

1. [Creación de una consulta](creating-a-query.md)
2. [Agregar contadores a la consulta](creating-a-query.md)
3. [Recopilación de los datos de rendimiento](collecting-performance-data.md)
4. [Mostrar los datos de rendimiento](displaying-performance-data.md)
5. [Cierre de la consulta](creating-a-query.md)

Puede recopilar datos de rendimiento de orígenes en tiempo real o archivos de registro. Para obtener más información sobre cómo escribir datos de rendimiento en archivos de registro, vea [Trabajar con archivos de registro](working-with-log-files.md).

## <a name="see-also"></a>Vea también

- [Recopilación de datos de rendimiento](collecting-performance-data.md)
- [Examinar contadores](browsing-counters.md)
- [Comprobación de valores devueltos de la interfaz PDH](checking-pdh-interface-return-values.md)
- [Ejemplos](examples.md)
