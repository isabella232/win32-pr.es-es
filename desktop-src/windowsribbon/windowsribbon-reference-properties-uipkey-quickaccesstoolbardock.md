---
title: UI_PKEY_QuickAccessToolbarDock
description: Identifica la propiedad \_ QuickAccessToolbarDock de PKEY de la \_ interfaz de usuario.
ms.assetid: 77f7b0a8-f276-4501-9d53-fb5a3185edcc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b9011cceb9b2ec96680ea3badd0ad40ae6121c14a70e065cfbfff5f5fe8e1f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118201388"
---
# <a name="ui_pkey_quickaccesstoolbardock"></a>UI \_ PKEY \_ QuickAccessToolbarDock

Identifica la propiedad \_ QuickAccessToolbarDock de PKEY de la \_ interfaz de usuario.

```
propertyDescription
   name = UI_PKEY_QuickAccessToolbarDock
   shellPKey = UI_PKEY_QuickAccessToolbarDock
   formatID = 00001002-7363-696e-8441798acf5aebb7
   propID = 1002
   typeInfo
      type = UI_CONTROLDOCK
```

## <a name="remarks"></a>Comentarios

La \_ interfaz de usuario \_ PKEY QuickAccessToolbarDock la usa una aplicación para consultar el estado de acoplamiento de la barra de herramientas de acceso rápido (QAT).

El valor de propiedad es de la [**\_ enumeración CONTROLDOCK de la**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) interfaz de usuario.



|    Enumeración                     |    Descripción                                                                                                                                                                                                                                                   |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UI \_ CONTROLDOCK \_ TOP    | El QAT se acopla en el área no cliente de la aplicación host de la cinta de opciones, como se muestra en la siguiente captura de pantalla.![captura de pantalla de la barra de herramientas de acceso rápido acoplada encima de la cinta de opciones en el área no cliente.](images/properties/qat-docktop.png)<br/> |
| UI \_ CONTROLDOCK \_ BOTTOM | El QAT se acopla como una banda visualmente integral debajo de la cinta de opciones, como se muestra en la siguiente captura de pantalla. ![captura de pantalla de la barra de herramientas de acceso rápido acoplada debajo de la cinta de opciones.](images/properties/qat-dockbottom.png)<br/>                           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades de la cinta de opciones](windowsribbon-reference-properties-ribbon.md)
</dt> </dl>

 

