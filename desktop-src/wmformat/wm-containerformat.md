---
title: WM/ContainerFormat
description: El atributo WM/ContainerFormat especifica el tipo de archivo que se carga en el objeto que realiza la llamada.
ms.assetid: fea5b2e4-f10d-4482-a7b3-7dabf58df085
keywords:
- Formato multimedia de Windows WM/ContainerFormat
topic_type:
- apiref
api_name:
- WM/ContainerFormat
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99e0d5cc430b0580c6719d212d664d8c19ddc65eee64e5877a8e6aba80d94a6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839445"
---
# <a name="wmcontainerformat"></a>WM/ContainerFormat

El **atributo WM/ContainerFormat** especifica el tipo de archivo que se carga en el objeto que realiza la llamada.

## <a name="global-constant"></a>Constante global

g \_ wszWMContainerFormat

## <a name="data-type"></a>Tipo de datos

[**WMT \_ STORAGE \_ FORMAT**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_storage_format) (**WMT TYPE \_ \_ BINARY**)

## <a name="remarks"></a>Comentarios

Este atributo se usa en lugar de **IWMProfile3::GetStorageFormat** e **IWMProfile3::SetStorageFormat**, que ya no se admiten.

Se trata de un atributo codificado.

Este atributo no se puede duplicar en el nivel de archivo. Si este atributo se usa para una secuencia individual, se tratará como metadatos personalizados y no transmitirá su significado normal a los objetos del SDK Windows Media Format.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




