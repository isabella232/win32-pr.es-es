---
title: UI_PKEY_QuickAccessToolbarDock
description: Identifica la propiedad \_ \_ QuickAccessToolbarDock de ui PKEY.
ms.assetid: 77f7b0a8-f276-4501-9d53-fb5a3185edcc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e28ec2e153755fd243bf78ee389cad40485a348
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443766"
---
# <a name="ui_pkey_quickaccesstoolbardock"></a>UI \_ PKEY \_ QuickAccessToolbarDock

Identifica la propiedad \_ \_ QuickAccessToolbarDock de ui PKEY.

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
| PARTE \_ INFERIOR DEL PANEL DE CONTROL DE INTERFAZ DE \_ USUARIO | El QAT se acopla como una banda visualmente integral debajo de la cinta de opciones, como se muestra en la siguiente captura de pantalla. ![captura de pantalla de la barra de herramientas de acceso rápido acoplada debajo de la cinta de opciones.](images/properties/qat-dockbottom.png)<br/>                           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades de la cinta de opciones](windowsribbon-reference-properties-ribbon.md)
</dt> </dl>

 

