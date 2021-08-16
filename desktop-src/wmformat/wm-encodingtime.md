---
title: WM/EncodingTime
description: El atributo WM/EncodingTime contiene una marca de tiempo de la hora a la que se codifica el contenido.
ms.assetid: 63da9392-264d-40bb-99fd-56db93801941
keywords:
- Formato multimedia de Windows WM/EncodingTime
topic_type:
- apiref
api_name:
- WM/EncodingTime
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20c76de789bd6ca88a9bbc2f3bb68381b3816524a07cbf97dc1a35b2526179a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118431848"
---
# <a name="wmencodingtime"></a>WM/EncodingTime

El **atributo WM/EncodingTime** contiene una marca de tiempo de la hora a la que se codifica el contenido.

## <a name="global-constant"></a>Constante global

g \_ wszWMEncodingTime

## <a name="data-type"></a>Tipo de datos

**FILETIME** (**WMT \_ TYPE \_ QWORD**)

## <a name="remarks"></a>Comentarios

Este atributo usa un valor FILETIME, que es un valor de 64 bits que representa el número de unidades de tiempo de 100 nanosegundos transcurridos desde el 1 de enero de 1601. Para obtener más información sobre FILETIME, consulte la Windows Información del sistema del SDK de plataforma.

No es un atributo codificado. Debe establecerlo manualmente si desea incluirlo en los archivos.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




