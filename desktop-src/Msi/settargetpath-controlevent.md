---
description: El evento SetTargetPath notifica al instalador que compruebe y establezca la ruta de acceso seleccionada. Si la ruta de acceso no es válida para escribirse, el instalador bloquea más ControlEvents asociados al control.
ms.assetid: 5649da99-1541-47ab-9d2e-b33a705998ec
title: SetTargetPath ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36812d291ab4410b08c577e6d118c3ff9e5dc0b4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272383"
---
# <a name="settargetpath-controlevent"></a>SetTargetPath ControlEvent

El evento SetTargetPath notifica al instalador que compruebe y establezca la ruta de acceso seleccionada. Si la ruta de acceso no es válida para escribirse, el instalador bloquea más ControlEvents asociados al control.

Este evento se puede publicar mediante un [control PushButton o](pushbutton-control.md)un [control SelectionTree](selectiontree-control.md). Este evento debe crearse en la [tabla ControlEvent](controlevent-table.md).

Este control ControlEvent requiere que la interfaz de usuario se ejecute en el [*nivel completo de la interfaz de*](f-gly.md) usuario. Este evento no funcionará con una interfaz de usuario [*reducida o*](r-gly.md) una interfaz de [*usuario básica.*](b-gly.md) Para obtener información, [vea Interfaz de usuario Levels](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

El instalador publica este control ControlEvent.

## <a name="argument"></a>Argumento

Nombre de la propiedad que contiene la ruta de acceso. Si la propiedad es indirecta, el nombre de la propiedad se incluye entre corchetes.

## <a name="action-on-subscribers"></a>Acción en suscriptores

Ninguno.

## <a name="typical-use"></a>Uso típico

Un control [PushButton](pushbutton-control.md) de un cuadro de diálogo examinar está asociado a este evento en la [tabla ControlEvent](controlevent-table.md) para comprobar la ruta de acceso seleccionada antes de volver al cuadro de diálogo de selección.

## <a name="remarks"></a>Observaciones

No intente configurar la ruta de acceso de destino si los componentes que usan esas rutas de acceso ya están instalados para el usuario actual o para otro usuario. Compruebe la [**propiedad ProductState**](productstate.md) antes de publicar SetTargetPath ControlEvent para determinar si el producto que contiene el componente está instalado.

 

 



