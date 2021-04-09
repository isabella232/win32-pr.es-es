---
title: WM/EncodingTime
description: El atributo WM/EncodingTime contiene una marca de tiempo de la hora a la que se ha codificado el contenido.
ms.assetid: 63da9392-264d-40bb-99fd-56db93801941
keywords:
- Formato de Windows Media WM/EncodingTime
topic_type:
- apiref
api_name:
- WM/EncodingTime
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d27119a9b54e3de22fe620f556c672bd4fe1a17
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076937"
---
# <a name="wmencodingtime"></a>WM/EncodingTime

El atributo **WM/EncodingTime** contiene una marca de tiempo de la hora a la que se ha codificado el contenido.

## <a name="global-constant"></a>Constante global

g \_ wszWMEncodingTime

## <a name="data-type"></a>Tipo de datos

**FILETIME** (**\_ tipo WMT \_ QWord**)

## <a name="remarks"></a>Observaciones

Este atributo usa un valor de FILETIME, que es un valor de 64 bits que representa el número de unidades de tiempo de 100-nanosegundos transcurridos desde el 1 de enero de 1601. Para obtener más información acerca de FILETIME, consulte la sección información del sistema de Windows del SDK de la plataforma.

No es un atributo codificado. Debe establecerlo manualmente si desea incluirlo en los archivos.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




