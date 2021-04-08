---
title: WM/WMShadowFileSourceDRMType (SDK de Windows Media Format 11)
description: El atributo WM/WMShadowFileSourceDRMType contiene el tipo de Rights Management que se usa para proteger el archivo original del que se deriva el archivo ASF.
ms.assetid: 58e7a383-6e80-42fc-bc75-5920dbe67a40
keywords:
- Formato de Windows Media WM/WMShadowFileSourceDRMType
topic_type:
- apiref
api_name:
- WM/WMShadowFileSourceDRMType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a0f33d961e8cd3645e4949980d91fe4de79119f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078756"
---
# <a name="wmwmshadowfilesourcedrmtype-windows-media-format-11-sdk"></a>WM/WMShadowFileSourceDRMType (SDK de Windows Media Format 11)

El atributo **WM/WMShadowFileSourceDRMType** contiene el tipo de Rights Management que se usa para proteger el archivo original del que se deriva el archivo ASF.

## <a name="global-constant"></a>Constante global

g \_ wszWMWMShadowFileSourceDRMType

## <a name="data-type"></a>Tipo de datos

**\_cadena de tipo WMT \_**

## <a name="remarks"></a>Observaciones

El contenido que se encuentra en un formato de archivo distinto de ASF y está protegido con algún tipo de administración de derechos se puede convertir en un archivo de Windows Media protegido por DRM de Windows Media a través de un proceso llamado importación de licencias. Este tipo de archivo ASF debe contener este atributo, así como WM/WMShadowFileSourceFileType, para realizar un seguimiento de la procedencia del contenido.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




