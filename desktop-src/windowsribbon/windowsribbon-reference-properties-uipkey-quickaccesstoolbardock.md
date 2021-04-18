---
title: UI_PKEY_QuickAccessToolbarDock
description: Identifica la propiedad QuickAccessToolbarDock de PKEY de la interfaz de usuario \_ \_ .
ms.assetid: 77f7b0a8-f276-4501-9d53-fb5a3185edcc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1ae48cb9ef2ee665739de2f3aacab197b461665
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420796"
---
# <a name="ui_pkey_quickaccesstoolbardock"></a>UI \_ PKEY \_ QuickAccessToolbarDock

Identifica la propiedad QuickAccessToolbarDock de PKEY de la interfaz de usuario \_ \_ .

```
propertyDescription
   name = UI_PKEY_QuickAccessToolbarDock
   shellPKey = UI_PKEY_QuickAccessToolbarDock
   formatID = 00001002-7363-696e-8441798acf5aebb7
   propID = 1002
   typeInfo
      type = UI_CONTROLDOCK
```

## <a name="remarks"></a>Observaciones

\_ \_ Una aplicación usa la interfaz de usuario PKEY QuickAccessToolbarDock para consultar el estado de acoplamiento de la barra de herramientas de acceso rápido (Qat).

El valor de la propiedad es de la enumeración [**\_ CONTROLDOCK**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) de la interfaz de usuario.



|                         |                                                                                                                                                                                                                                                       |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CONTROLDOCK de IU \_ \_ superior    | El QAT se acopla en el área no cliente de la aplicación host de la cinta de opciones, como se muestra en la siguiente captura de pantalla.![captura de pantalla de la barra de herramientas de acceso rápido acoplada encima de la cinta de opciones en el área no cliente.](images/properties/qat-docktop.png)<br/> |
| CONTROLDOCK de IU \_ \_ inferior | El QAT se acopla como una banda entera visualmente debajo de la cinta de opciones, como se muestra en la siguiente captura de pantalla. ![captura de pantalla de la barra de herramientas de acceso rápido acoplada debajo de la cinta de opciones.](images/properties/qat-dockbottom.png)<br/>                           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades de la cinta](windowsribbon-reference-properties-ribbon.md)
</dt> </dl>

 

