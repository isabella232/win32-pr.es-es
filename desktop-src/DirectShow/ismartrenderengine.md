---
description: La interfaz ISmartRenderEngine proporciona métodos que admiten la recompresión inteligente en DirectShow Editing Services (DES). El motor de representación inteligente expone esta interfaz.
ms.assetid: 0e03708f-e471-4188-a212-ec5e951d20fa
title: Interfaz ISmartRenderEngine (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4e82ba73764adc27ff366533c3b5cfdc2eebc7e3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063234"
---
# <a name="ismartrenderengine-interface"></a>Interfaz ISmartRenderEngine

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

La `ISmartRenderEngine` interfaz proporciona métodos que admiten la recompresión inteligente [en DirectShow Editing Services](directshow-editing-services.md) (DES). El motor de representación inteligente expone esta interfaz.

## <a name="members"></a>Members

La **interfaz ISmartRenderEngine** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ISmartRenderEngine** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ISmartRenderEngine** tiene estos métodos.



| Método                                                                | Descripción                                                                          |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**GetGroupCompressor**](ismartrenderengine-getgroupcompressor.md)   | Recupera el filtro de compresión para el grupo especificado.<br/>                 |
| [**SetFindCompressorCB**](ismartrenderengine-setfindcompressorcb.md) | Sin implementar.<br/>                                                          |
| [**SetGroupCompressor**](ismartrenderengine-setgroupcompressor.md)   | Especifica un filtro de compresión que se usará al representar el grupo especificado.<br/> |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Representación de un Project](rendering-a-project.md)
</dt> </dl>

 

 
