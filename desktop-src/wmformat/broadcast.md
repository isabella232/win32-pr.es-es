---
title: Difusión
description: El atributo Broadcast es un atributo de nivel de archivo que indica si se puede difundir el contenido. Se supone que todo el contenido para el que no se ha asignado ningún copyright se puede difundir legalmente.
ms.assetid: da2adf16-a9b5-4678-896e-2be8f5ca27e4
keywords:
- Difundir formato de Windows Media
topic_type:
- apiref
api_name:
- Broadcast
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbf9e7d94682f8dbf08850f87954a934fd909afe
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105704863"
---
# <a name="broadcast"></a>Difusión

El atributo **Broadcast** es un atributo de nivel de archivo que indica si se puede difundir el contenido. Se supone que todo el contenido para el que no se ha asignado ningún copyright se puede difundir legalmente.

## <a name="global-constant"></a>Constante global

g \_ wszWMBroadcast

## <a name="data-type"></a>Tipo de datos

**tipo de WMT \_ \_ bool**

## <a name="remarks"></a>Observaciones

Se trata de un atributo codificado.

Este atributo no se puede duplicar en el nivel de archivo. Si este atributo se usa para una secuencia individual, se tratará como metadatos personalizados y no enviará su significado normal a los objetos del SDK de Windows Media Format.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




