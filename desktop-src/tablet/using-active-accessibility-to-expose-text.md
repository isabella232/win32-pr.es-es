---
description: Información general sobre el uso de la accesibilidad activa para exponer texto.
ms.assetid: c04ade90-5f17-4e16-b82b-c99230000954
title: Usar Active Accessibility para exponer texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52d475a8c576e109f47be7b5a3d61cddf543038d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467143"
---
# <a name="using-active-accessibility-to-expose-text"></a>Usar Active Accessibility para exponer texto

Las aplicaciones pueden usar Microsoft Active Accessibility para exponer texto. Sin embargo, la [**interfaz IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible) definida por versiones anteriores de Active Accessibility no está optimizada para exponer grandes cantidades de texto enriquecido. Las versiones posteriores definen interfaces optimizadas para exponer grandes cantidades de atributos de texto y texto.

Para exponer grandes cantidades de texto, cree objetos independientes del Modelo de objetos componentes (COM) que [**admitan IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible)o elementos secundarios, para representar cada ejecución de texto. Una ejecución es una línea, o parte de una línea, que comparte el mismo formato.

Active Accessibility solo expone el texto y su ubicación, pero no tiene ningún mecanismo para exponer el formato del texto. A pesar de estas limitaciones, algunos programas usan Active Accessibility para exponer texto. Por ejemplo, Microsoft Internet Explorer y Microsoft Visual Studio usan Active Accessibility para exponer grandes cantidades de texto.

Para obtener más información sobre cómo exponer texto mediante Active Accessibility, vea [Accesibilidad.](../accessibility/accessibility.md)

 

 
