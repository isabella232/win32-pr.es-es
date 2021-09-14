---
title: External.SelectedTaskPane
description: Nota En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. La propiedad SelectedTaskPane especifica o recupera el panel de tareas seleccionado actualmente.
ms.assetid: af7b4627-1336-444c-9b4e-5f2e07d9eea7
keywords:
- External.SelectedTaskPane Reproductor de Windows Media
topic_type:
- apiref
api_name:
- External.SelectedTaskPane
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28535e0497362a2153bcaad439425174e9c1bdc1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241833"
---
# <a name="externalselectedtaskpane"></a>External.SelectedTaskPane

> [!Note]  
> En este tema se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

La **propiedad SelectedTaskPane** especifica o recupera el panel de tareas seleccionado actualmente.

## <a name="syntax"></a>Sintaxis

window.external.SelectedTaskPane = *servicetask*

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una cadena de lectura y **escritura.** Los valores posibles son "ServiceTask1", "ServiceTask2" y "ServiceTask3".

## <a name="remarks"></a>Observaciones

Al especificar un valor para esta propiedad, se resalta el botón de ese panel. No activa el panel de tareas especificado. Debe especificar un valor para esta propiedad para establecer el botón del panel de tareas actual de la página web cuando se cargue la página para asegurarse de que el botón del panel de tareas correcto está activo.

Para que un panel de tareas determinado sea el activo, use el **método NavigateTaskPaneURL.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 10 o posterior<br/>                                        |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto externo para almacenes en línea de tipo 2**](external-object-for-type-2-online-stores.md)
</dt> <dt>

[**External.NavigateTaskPaneURL**](external-navigatetaskpaneurl.md)
</dt> </dl>

 

 





