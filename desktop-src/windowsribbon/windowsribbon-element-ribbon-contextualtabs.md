---
title: Propiedad Ribbon. ContextualTabs
description: Representa un contenedor para las pestañas contextuales.
ms.assetid: 1f57a8d7-97ac-4007-8a36-c6aec5b85e6c
keywords:
- Ribbon. ContextualTabs (propiedad) cinta de Windows
topic_type:
- apiref
api_name:
- Ribbon.ContextualTabs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 790a7c93df71ab5117b591367c6b80fc0f8a748d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801550"
---
# <a name="ribboncontextualtabs-property"></a>Propiedad Ribbon. ContextualTabs

Representa un contenedor para las pestañas contextuales.

## <a name="usage"></a>Uso

``` syntax
<Ribbon.ContextualTabs>
  child elements
</Ribbon.ContextualTabs>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                       | Descripción                                     |
|---------------------------------------------------------------|-------------------------------------------------|
| [**TabGroup**](windowsribbon-element-tabgroup.md)<br/> | Debe aparecer al menos una vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                   |
|-----------------------------------------------------------|
| [**Cinta de opciones**](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a>Observaciones

Opcional.

Puede producirse al menos una vez para cada [**cinta**](windowsribbon-element-ribbon.md)de opciones.

Las pestañas contextuales son útiles para mostrar funciones que solo son relevantes para un contexto de aplicación específico, como una pestaña formato de imagen en un editor de texto que solo se muestra cuando se resalta una imagen. Normalmente, las pestañas contextuales no son visibles hasta que se produce un contexto de aplicación específico y la aplicación notifica al marco de la cinta de opciones.

Cuando se muestra, las pestañas contextuales están codificadas por colores para diferenciarlas de las pestañas normales.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico para el elemento **Ribbon. ContextualTabs** .

En esta sección de código se muestra una declaración de comandos de [**TabGroup**](windowsribbon-element-tabgroup.md) y dos declaraciones de comandos de [**pestaña**](windowsribbon-element-tab.md) contextuales.


```XML
<!-- Contextual Tabs -->
<Command Name='cmdContextualTab1'
         LabelTitle='Contextual Tab 1'
         Symbol='ID_CONTEXTUALTAB1'/>
<Command Name='cmdContextualTab2'
         LabelTitle='Contextual Tab 2'
         Symbol='ID_CONTEXTUALTAB2'/>
<Command Name='cmdContextualTabGroup'
         LabelTitle='Contextual Tabs'
         Symbol='ID_CONTEXTUALTAB_GROUP'/>
```



En esta sección de código se muestra la declaración de control **Ribbon. ContextualTabs** con un [**TabGroup**](windowsribbon-element-tabgroup.md) y dos controles de [**ficha**](windowsribbon-element-tab.md) contextuales.


```XML
      <Ribbon.ContextualTabs>
        <TabGroup CommandName='cmdContextualTabGroup'>
          <Tab CommandName='cmdContextualTab1'>
            <!--InRibbonGallery Group-->
            <Group CommandName='cmdInRibbonGalleryGroup'
                   SizeDefinition='OneInRibbonGallery'>
              <InRibbonGallery CommandName='cmdTextSizeGallery3'
                               HasLargeItems='true'
                               ItemHeight='32'
                               ItemWidth='32'
                               MaxColumns='3' >
                <InRibbonGallery.MenuLayout>
                  <FlowMenuLayout Columns='3'
                                  Gripper ='Corner'/>
                </InRibbonGallery.MenuLayout>
              </InRibbonGallery>
            </Group>
            <!--Command Galleries Group-->
            <Group CommandName='cmdCommandGalleriesGroup'
                   SizeDefinition='OneInRibbonGallery'>
              <InRibbonGallery CommandName='cmdCommandGallery1'
                               Type='Commands'
                               MaxRows='3'
                               MaxColumns='3'>
                <InRibbonGallery.MenuLayout>
                  <FlowMenuLayout Columns='3'
                                  Gripper ='Corner'/>
                </InRibbonGallery.MenuLayout>
              </InRibbonGallery>
            </Group>
          </Tab>
          <Tab CommandName='cmdContextualTab2'></Tab>
        </TabGroup>
      </Ribbon.ContextualTabs> 
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Cinta. pestañas**](windowsribbon-element-ribbon-tabs.md)
</dt> </dl>

 

 





