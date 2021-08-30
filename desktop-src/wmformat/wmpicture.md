---
title: WM/Picture
description: El atributo WM/Picture contiene una imagen relacionada con el contenido.
ms.assetid: ec82dfdf-7755-4758-9771-096aac114f78
keywords:
- Formato multimedia de las ventanas WM/Picture
topic_type:
- apiref
api_name:
- WM/Picture
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c0648cc82faae7a0bab9614761caef98c316fd73b5eb90550d14754386282f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109935"
---
# <a name="wmpicture"></a>WM/Picture

El **atributo WM/Picture** contiene una imagen relacionada con el contenido.

## <a name="global-constant"></a>Constante global

g \_ wszWMPicture

## <a name="data-type"></a>Tipo de datos

[**WM \_ PICTURE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) (**WMT \_ TYPE \_ BINARY**)

## <a name="remarks"></a>Comentarios

Este atributo es compatible con el marco ID3, APIC. La especificación ID3 para el marco de APIC establece que, aunque puede haber cualquier número de fotogramas de APIC asociados a un archivo, solo uno puede ser de tipo 1 y solo uno puede ser de tipo 2. La especificación también indica que la descripción de la imagen no puede tener más de 64 caracteres, pero puede estar vacía.

Los atributos WM/Picture agregados con los objetos del SDK Windows Media Format no se validan automáticamente para ajustarse a las especificaciones de ID3. Debe agregar código en la aplicación para realizar validaciones si desea mantener la compatibilidad completa con ID3.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> <dt>

[**IMAGEN \_ DE WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture)
</dt> </dl>

 

 




