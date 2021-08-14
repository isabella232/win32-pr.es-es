---
title: Propiedad Ribbon.QuickAccessToolbar
description: Representa un contenedor para la barra de herramientas de acceso rápido (QAT).
ms.assetid: 8a873a48-4f8b-439d-acad-7da2081fbf40
keywords:
- Cinta de opciones de la propiedad Ribbon.QuickAccessToolbar Windows cinta de opciones
topic_type:
- apiref
api_name:
- Ribbon.QuickAccessToolbar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83e1fa4cb5de43be2b7316d4ed1786c2a1325fa4468538e2ffea41d5d8c9ef0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118202322"
---
# <a name="ribbonquickaccesstoolbar-property"></a>Propiedad Ribbon.QuickAccessToolbar

Representa un contenedor para la barra de herramientas de acceso rápido (QAT).

## <a name="usage"></a>Uso

``` syntax
<Ribbon.QuickAccessToolbar>
  child elements
</Ribbon.QuickAccessToolbar>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                           | Descripción                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md)<br/> | Debe producirse exactamente una vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                   |
|-----------------------------------------------------------|
| [**Cinta de opciones**](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a>Comentarios

Obligatorio.

Puede producirse una o varias veces para cada cinta [**de opciones.**](windowsribbon-element-ribbon.md)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico para el **elemento Ribbon.QuickAccessToolbar.**


```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/> |



 

 





