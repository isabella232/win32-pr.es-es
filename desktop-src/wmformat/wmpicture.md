---
title: WM/imagen
description: El atributo WM/imagen contiene una imagen relacionada con el contenido.
ms.assetid: ec82dfdf-7755-4758-9771-096aac114f78
keywords:
- Formato de Windows Media WM/imagen
topic_type:
- apiref
api_name:
- WM/Picture
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ba3f74378112c8e3f58958db8b22c970e8e099
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103994706"
---
# <a name="wmpicture"></a>WM/imagen

El atributo **WM/imagen** contiene una imagen relacionada con el contenido.

## <a name="global-constant"></a>Constante global

g \_ wszWMPicture

## <a name="data-type"></a>Tipo de datos

[**WM \_ IMAGEN**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) (**\_ tipo WMT \_ binario**)

## <a name="remarks"></a>Observaciones

Este atributo es compatible con el marco ID3, APIC. La especificación ID3 del marco APIC estipula que, aunque puede haber cualquier número de Marcos APIC asociados a un archivo, solo uno puede ser de tipo 1 y solo uno puede ser de tipo 2. La especificación también indica que la descripción de la imagen no puede tener más de 64 caracteres, pero puede estar vacía.

Los atributos de WM/imagen agregados con los objetos del SDK de Windows Media Format no se validan automáticamente para ajustarse a las especificaciones ID3. Debe agregar código en la aplicación para realizar validaciones si desea mantener la compatibilidad completa con ID3.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> <dt>

[**imagen de WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture)
</dt> </dl>

 

 




