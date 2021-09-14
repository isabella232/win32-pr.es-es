---
description: Devolución de llamada para que el usuario registre una plantilla de archivo .x.
ms.assetid: 60568556-704c-4be3-bbde-04887583cf70
title: Método ID3DXSaveUserData::RegisterTemplates (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.RegisterTemplates
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c1465b76b758f6a5ed9e7dff4c7126935fb7c5d1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966644"
---
# <a name="id3dxsaveuserdataregistertemplates-method"></a>Método ID3DXSaveUserData::RegisterTemplates

Devolución de llamada para que el usuario registre una plantilla de archivo .x.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RegisterTemplates(
  [in] LPD3DXFILE pXFileApi
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pXFileApi* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXFILE**](id3dxfile.md)**

Use este puntero para registrar plantillas de archivo .x definidas por el usuario. Vea [**ID3DXFile**](id3dxfile.md). No use este parámetro para agregar objetos de datos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Los valores devueltos de este método los implementa un programador de aplicaciones. En general, si no se produce ningún error, programe el método para devolver D3D \_ OK. De lo contrario, programe el método para devolver un mensaje de error adecuado de [D3DERR](d3derr.md) o [**D3DXERR**](./d3dxerr.md), ya que esto hará que [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) también devuelva el error.

## <a name="remarks"></a>Observaciones

**ID3DXSaveUserData::RegisterTemplates** e [**ID3DXSaveUserData::SaveTemplates**](id3dxsaveuserdata--savetemplates.md) proporcionan un mecanismo para agregar una plantilla a un archivo .x para guardar datos de usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXSaveUserData](id3dxsaveuserdata.md)
</dt> </dl>

 

 
