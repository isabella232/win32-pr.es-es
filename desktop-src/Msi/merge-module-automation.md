---
description: Mergemod.dll proporciona un objeto COM que implementa operaciones de combinación y generación de imágenes de origen para módulos de combinación. El objeto principal implementa interfaces para programas de C/C++ y clientes de automatización, incluidos Visual Basic y VBScript.
ms.assetid: 877d3691-948f-4aea-89d8-0ff008126ccc
title: Automatización de módulos de mezcla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ae27370b2ad898cf9413567285afc41d117815
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074384"
---
# <a name="merge-module-automation"></a>Automatización de módulos de mezcla

Mergemod.dll proporciona un objeto COM que implementa operaciones de combinación y generación de imágenes de origen para módulos de combinación. El objeto principal implementa interfaces para programas de C/C++ y clientes de automatización, incluidos Visual Basic y VBScript.

El método preferido para instalar Mergemod.dll es mediante Windows Installer. El identificador de componente del componente que contiene la interfaz COM de Mergemod.dll es {FD153241-37EC-11D2-8892-00A0C981B015}. El mismo archivo binario se puede usar en todos los sistemas Windows y el archivo DLL se registrará por sí mismo a través de regsvr32 en sistemas anteriores.

Tenga en Mergemod.dll requiere que el Msvcrt.dll esté instalado en el sistema.

Tenga en cuenta Mergemod.dll 2.0 es necesario para crear módulos de [combinación configurables.](configurable-merge-modules.md) Mergemod.dll versión 2.0 proporciona funcionalidad extendida en tiempo de compilación a través de la [**interfaz IMsmMerge2.**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) Este CLSID admite toda la funcionalidad existente de la [**interfaz IMsmMerge**](/windows/win32/api/mergemod/nn-mergemod-imsmmerge) proporcionada por Mergemod.dll versión 1.0. La interfaz predeterminada en el objeto [**Merge**](merge-object.md) de Mergemod.dll 2.0 es la **interfaz IMsmMerge2** en lugar de la **interfaz IMsmMerge.**

[Modelo de objetos para Mergemod.dll versión 1.0](object-model-for-mergemod-dll-version-1-0.md)

[Modelo de objetos para Mergemod.dll versión 2.0](object-model-for-mergemod-dll-version-2-0.md)

 

 
