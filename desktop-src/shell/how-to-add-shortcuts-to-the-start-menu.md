---
description: Para agregar un elemento al submenú Programas, siga estos pasos.
ms.assetid: F8793C33-2281-4E4A-9659-4189E1C8279A
title: Cómo agregar accesos directos al menú Inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77ee942e07c48ed7addf07160412008bfb5b9322
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572521"
---
# <a name="how-to-add-shortcuts-to-the-start-menu"></a>Cómo agregar accesos directos al menú Inicio

Para agregar un elemento al **submenú Programas,** siga estos pasos.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Paso 1:

Cree un [vínculo de shell](./links.md) mediante la interfaz [**IShellLink.**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka)

### <a name="step-2"></a>Paso 2:

Obtenga la ubicación de la carpeta Programas mediante la función [**SHGetKnownFolderPath,**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) pasando [**los programas FOLDERID \_**](knownfolderid.md).

### <a name="step-3"></a>Paso 3:

Agregue el vínculo shell a la carpeta Programas. También puede crear una carpeta en la carpeta Programas y agregar el vínculo a esa carpeta.

 

 
