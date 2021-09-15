---
title: Difusión
description: El atributo Broadcast es un atributo de nivel de archivo que indica si el contenido se puede difundir. Se supone que cualquier contenido para el que no se haya asignado ningún copyright se puede difundir legalmente.
ms.assetid: da2adf16-a9b5-4678-896e-2be8f5ca27e4
keywords:
- Formato multimedia de difusión de ventanas
topic_type:
- apiref
api_name:
- Broadcast
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbf9e7d94682f8dbf08850f87954a934fd909afe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467108"
---
# <a name="broadcast"></a>Difusión

El **atributo Broadcast** es un atributo de nivel de archivo que indica si el contenido se puede difundir. Se supone que cualquier contenido para el que no se haya asignado ningún copyright se puede difundir legalmente.

## <a name="global-constant"></a>Constante global

g \_ wszWMBroadcast

## <a name="data-type"></a>Tipo de datos

**WMT \_ TYPE \_ BOOL**

## <a name="remarks"></a>Observaciones

Se trata de un atributo codificado.

Este atributo no se puede duplicar en el nivel de archivo. Si este atributo se usa para una secuencia individual, se tratará como metadatos personalizados y no transmitirá su significado normal a los objetos del SDK Windows Media Format.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




