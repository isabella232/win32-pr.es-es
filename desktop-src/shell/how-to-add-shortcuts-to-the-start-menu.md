---
description: Para agregar un elemento al submenú programas, siga estos pasos.
ms.assetid: F8793C33-2281-4E4A-9659-4189E1C8279A
title: Cómo agregar accesos directos al menú Inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77ee942e07c48ed7addf07160412008bfb5b9322
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156476"
---
# <a name="how-to-add-shortcuts-to-the-start-menu"></a>Cómo agregar accesos directos al menú Inicio

Para agregar un elemento al submenú **programas** , siga estos pasos.

## <a name="instructions"></a>Instrucciones

### <a name="step-1"></a>Paso 1:

Cree un [vínculo de Shell](./links.md) mediante la interfaz [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) .

### <a name="step-2"></a>Paso 2:

Obtenga la ubicación de la carpeta programas mediante la función [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) , pasando [**FOLDERID \_ programas**](knownfolderid.md).

### <a name="step-3"></a>Paso 3:

Agregue el vínculo de Shell a la carpeta programas. También puede crear una carpeta en la carpeta programas y agregar el vínculo a esa carpeta.

 

 
