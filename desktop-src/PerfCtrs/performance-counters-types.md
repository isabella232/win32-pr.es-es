---
description: PDH define los siguientes tipos de datos.
ms.assetid: 8a2e8683-502a-4893-8b4f-5e2cf464a933
title: Tipos de datos de contadores de rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38f9800288494eb82f675265b6e0b801c783668d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169150"
---
# <a name="performance-counters-data-types"></a>Tipos de datos de contadores de rendimiento

## <a name="performance-data-helper-pdh-types"></a>Tipos del asistente de datos de rendimiento (PDH)

Los consumidores que usan las funciones del asistente de datos [de rendimiento (PDH)](using-the-pdh-functions-to-consume-counter-data.md) usan los siguientes tipos:

| Tipo de datos | Descripción
|-----------|------------
| **PDH \_ HQUERY**   | Identificador de una consulta. La [**función PdhOpenQuery**](/windows/win32/api/pdh/nf-pdh-pdhopenqueryw) devuelve este identificador. Cierre el identificador mediante [**PdhCloseQuery**](/windows/win32/api/pdh/nf-pdh-pdhclosequery).
| **PDH \_ HCOUNTER** | Identificador de un contador. La [**función PdhAddCounter**](/windows/win32/api/pdh/nf-pdh-pdhaddcounterw) devuelve este identificador. Cierre el identificador mediante [**PdhRemoveCounter**](/windows/win32/api/pdh/nf-pdh-pdhremovecounter) o cierre el identificador a la consulta que contiene el contador. No llame a **PdhRemoveCounter en** un contador si la consulta correspondiente ya se ha cerrado. PDH mantiene la vinculación entre contadores y consultas y cerrará automáticamente los identificadores de contador cuando se cierre el identificador de consulta correspondiente.
| **PDH \_ HLOG**     | Identificador de un archivo de registro. Las [**funciones PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga) [**y PdhBindInputDataSource**](/windows/desktop/api/Pdh/nf-pdh-pdhbindinputdatasourcea) devuelven este identificador. Cierre el identificador mediante [**PdhCloseLog.**](/windows/win32/api/pdh/nf-pdh-pdhcloselog)
| **ESTADO DE \_ PDH**   | Valor de estado de PDH. Todas las funciones de PDH devuelven un valor de tipo **PDH \_ STATUS**. Si la función se realiza correctamente, el valor devuelto es ERROR \_ SUCCESS. De lo contrario, la función devuelve [un código de error del sistema](/windows/desktop/Debug/system-error-codes) o un código de error [PDH](pdh-error-codes.md).
