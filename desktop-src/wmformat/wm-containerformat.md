---
title: WM/ContainerFormat
description: El atributo WM/ContainerFormat especifica el tipo de archivo que se carga en el objeto que realiza la llamada.
ms.assetid: fea5b2e4-f10d-4482-a7b3-7dabf58df085
keywords:
- Formato de Windows Media WM/ContainerFormat
topic_type:
- apiref
api_name:
- WM/ContainerFormat
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9394fca14c3e07eb1f867c7b8ac473b2b61a9a2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784127"
---
# <a name="wmcontainerformat"></a>WM/ContainerFormat

El atributo **WM/ContainerFormat** especifica el tipo de archivo que se carga en el objeto que realiza la llamada.

## <a name="global-constant"></a>Constante global

g \_ wszWMContainerFormat

## <a name="data-type"></a>Tipo de datos

[**WMT \_ \_formato de almacenamiento**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_storage_format) (**\_ tipo WMT \_ binario**)

## <a name="remarks"></a>Observaciones

Este atributo se usa en lugar de **IWMProfile3:: GetStorageFormat** y **IWMProfile3:: SetStorageFormat**, que ya no se admiten.

Se trata de un atributo codificado.

Este atributo no se puede duplicar en el nivel de archivo. Si este atributo se usa para una secuencia individual, se tratará como metadatos personalizados y no enviará su significado normal a los objetos del SDK de Windows Media Format.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




