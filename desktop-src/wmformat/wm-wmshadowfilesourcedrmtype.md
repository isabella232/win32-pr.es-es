---
title: WM/WMShadowFileSourceDRMType (Windows SDK de formato multimedia 11)
description: El atributo WM/WMShadowFileSourceDRMType contiene el tipo de rights management que se usa para proteger el archivo original del que se deriva el archivo ASF.
ms.assetid: 58e7a383-6e80-42fc-bc75-5920dbe67a40
keywords:
- Formato multimedia de Windows WM/WMShadowFileSourceDRMType
topic_type:
- apiref
api_name:
- WM/WMShadowFileSourceDRMType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85c7ea97d2388b402bd05f67c1d8f7bf417c69a6853b3485e2cf0484cedcbc5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118698151"
---
# <a name="wmwmshadowfilesourcedrmtype-windows-media-format-11-sdk"></a>WM/WMShadowFileSourceDRMType (Windows SDK de formato multimedia 11)

El **atributo WM/WMShadowFileSourceDRMType** contiene el tipo de rights management que se usa para proteger el archivo original del que se deriva el archivo ASF.

## <a name="global-constant"></a>Constante global

g \_ wszWMWMShadowFileSourceDRMType

## <a name="data-type"></a>Tipo de datos

**CADENA DE \_ TIPO \_ WMT**

## <a name="remarks"></a>Comentarios

El contenido que existe en un formato de archivo distinto de ASF y que está protegido con algún tipo de administración de derechos se puede convertir en un archivo multimedia de Windows protegido por drm multimedia de Windows a través de un proceso denominado importación de licencias. Este tipo de archivo ASF debe contener este atributo, así como WM/WMShadowFileSourceFileType para realizar un seguimiento de dónde provenía el contenido.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




