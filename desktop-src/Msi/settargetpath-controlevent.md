---
description: El evento SetTargetPath notifica al instalador que compruebe y establezca la ruta de acceso seleccionada. Si la ruta de acceso no es válida en la que se va a escribir, el instalador bloquea más ControlEvents asociadas al control.
ms.assetid: 5649da99-1541-47ab-9d2e-b33a705998ec
title: SetTargetPath ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36812d291ab4410b08c577e6d118c3ff9e5dc0b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277739"
---
# <a name="settargetpath-controlevent"></a>SetTargetPath ControlEvent,

El evento SetTargetPath notifica al instalador que compruebe y establezca la ruta de acceso seleccionada. Si la ruta de acceso no es válida en la que se va a escribir, el instalador bloquea más ControlEvents asociadas al control.

Este evento puede ser publicado por un [control Pushbutton](pushbutton-control.md)o un [control SelectionTree](selectiontree-control.md). Este evento se debe crear en la [tabla ControlEvent,](controlevent-table.md).

Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) . Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida. Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

Este ControlEvent, lo publica el instalador.

## <a name="argument"></a>Argumento

Nombre de la propiedad que contiene la ruta de acceso. Si la propiedad está indirecta, el nombre de la propiedad se incluye entre corchetes.

## <a name="action-on-subscribers"></a>Acción en los suscriptores

Ninguno.

## <a name="typical-use"></a>Uso típico

Un control [Pushbutton](pushbutton-control.md) en un cuadro de diálogo de exploración está asociado a este evento en la tabla [ControlEvent,](controlevent-table.md) para comprobar la ruta de acceso seleccionada antes de volver al cuadro de diálogo de selección.

## <a name="remarks"></a>Observaciones

No intente configurar la ruta de acceso de destino si los componentes que usan esas rutas ya están instalados para el usuario actual o para otro usuario. Compruebe la propiedad [**ProductState**](productstate.md) antes de publicar el SetTargetPath ControlEvent, para determinar si el producto que contiene el componente está instalado.

 

 



