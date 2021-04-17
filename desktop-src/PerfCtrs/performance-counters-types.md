---
description: PDH define los siguientes tipos de datos.
ms.assetid: 8a2e8683-502a-4893-8b4f-5e2cf464a933
title: Tipos de datos de contadores de rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38f9800288494eb82f675265b6e0b801c783668d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667268"
---
# <a name="performance-counters-data-types"></a>Tipos de datos de contadores de rendimiento

## <a name="performance-data-helper-pdh-types"></a>Tipos de aplicación auxiliar de datos de rendimiento (PDH)

Los consumidores que usan las funciones del [ayudante de datos de rendimiento (PDH)](using-the-pdh-functions-to-consume-counter-data.md) usan los siguientes tipos:

| Tipo de datos | Descripción
|-----------|------------
| **HQUERY de PDH \_**   | Identificador de una consulta. La función [**PdhOpenQuery**](/windows/win32/api/pdh/nf-pdh-pdhopenqueryw) devuelve este identificador. Cierre el controlador mediante [**PdhCloseQuery**](/windows/win32/api/pdh/nf-pdh-pdhclosequery).
| **HCOUNTER de PDH \_** | Identificador de un contador. La función [**PdhAddCounter**](/windows/win32/api/pdh/nf-pdh-pdhaddcounterw) devuelve este identificador. Cierre el identificador mediante [**PdhRemoveCounter**](/windows/win32/api/pdh/nf-pdh-pdhremovecounter) o cerrando el identificador de la consulta que contiene el contador. No llame a **PdhRemoveCounter** en un contador si la consulta correspondiente ya se ha cerrado. PDH mantiene la vinculación entre contadores y consultas, y cerrará automáticamente los identificadores de contador cuando se cierre el identificador de consulta correspondiente.
| **HLOG de PDH \_**     | Identificador de un archivo de registro. Las funciones [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga) y [**PdhBindInputDataSource**](/windows/desktop/api/Pdh/nf-pdh-pdhbindinputdatasourcea) devuelven este identificador. Cierre el controlador mediante [**PdhCloseLog**](/windows/win32/api/pdh/nf-pdh-pdhcloselog).
| **Estado de PDH \_**   | Valor de estado de PDH. Todas las funciones PDH devuelven un valor de tipo **PDH \_ status**. Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success. De lo contrario, la función devuelve un [código de error del sistema](/windows/desktop/Debug/system-error-codes) o un [código de error de PDH](pdh-error-codes.md).
