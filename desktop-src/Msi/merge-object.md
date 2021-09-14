---
description: El objeto Merge proporciona acceso a otros objetos de nivel superior. Se debe crear un objeto Merge antes de cargar la compatibilidad de automatización requerida por COM para acceder a las funciones de Mergemod.dll.
ms.assetid: 3f76ee8a-d195-4a69-99a3-31ef2c1c72d5
title: Objeto Merge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1379202d4f252560a381f8af09b30741faa060ce
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074385"
---
# <a name="merge-object"></a>Objeto Merge

El **objeto Merge** proporciona acceso a otros objetos de nivel superior. Se **debe crear** un objeto Merge antes de cargar la compatibilidad de automatización requerida por COM para acceder a las funciones de Mergemod.dll.

Mergemod.dll proporciona acceso a la funcionalidad extendida en tiempo de compilación a través de una segunda versión del CLSID existente. Este CLSID admite la funcionalidad existente disponible a través de la interfaz [**IMsmMerge,**](/windows/win32/api/mergemod/nn-mergemod-imsmmerge) pero la interfaz predeterminada en el objeto (y la interfaz dual asociada) es la interfaz [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) en lugar de la interfaz **IMsmMerge.**

 

 
