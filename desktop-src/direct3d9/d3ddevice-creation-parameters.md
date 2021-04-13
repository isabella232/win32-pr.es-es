---
description: Describe los parámetros de creación de un dispositivo.
ms.assetid: 7db5ef2b-6894-4113-b726-8b238bb4fb2f
title: D3DDEVICE_CREATION_PARAMETERS estructura (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVICE_CREATION_PARAMETERS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 72b2f35f1666ec2095c6ea8f5d5588dc7fd62f2c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362494"
---
# <a name="d3ddevice_creation_parameters-structure"></a>\_Estructura de \_ los parámetros de creación de D3DDEVICE

Describe los parámetros de creación de un dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DDEVICE_CREATION_PARAMETERS {
  UINT       AdapterOrdinal;
  D3DDEVTYPE DeviceType;
  HWND       hFocusWindow;
  DWORD      BehaviorFlags;
} D3DDEVICE_CREATION_PARAMETERS, *LPD3DDEVICE_CREATION_PARAMETERS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**AdapterOrdinal**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número ordinal que denota el adaptador de pantalla. D3DADAPTER \_ default siempre es el adaptador de pantalla principal. Use este ordinal como parámetro del adaptador para cualquiera de los métodos [**IDirect3D9**](/windows/desktop/api) . Tenga en cuenta que las diferentes instancias de objetos de Direct3D 9,0 pueden utilizar distintos ordinales. Los adaptadores pueden escribir o dejar un sistema cuando los usuarios, por ejemplo, agregan o quitan monitores de un sistema de varios monitores o cuando intercambian a un portátil. Por lo tanto, use este ordinal solo en una instancia de Direct3D 9,0 conocida como válida, es decir, el Direct3D 9,0 que creó esta interfaz [**IDirect3DDevice9**](/windows/desktop/api) o el Direct3D 9,0 devuelto desde [**GetDirect3D**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdirect3d), como se llama a través de esta interfaz **IDirect3DDevice9** .

</dd> <dt>

**DeviceType**
</dt> <dd>

Tipo: **[ **D3DDEVTYPE**](./d3ddevtype.md)**

</dd> <dd>

Miembro del tipo enumerado [**D3DDEVTYPE**](./d3ddevtype.md) . Denota la cantidad de funcionalidad emulada para este dispositivo. El valor de este parámetro refleja el valor pasado a la llamada a [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) que creó este dispositivo.

</dd> <dt>

**hFocusWindow**
</dt> <dd>

Tipo: **[ **hWnd**](../winprog/windows-data-types.md)**

</dd> <dd>

Identificador de ventana al que pertenece el foco para este dispositivo Direct3D. El valor de este parámetro refleja el valor pasado a la llamada a [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) que creó este dispositivo.

</dd> <dt>

**BehaviorFlags**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Combinación de una o varias constantes de [D3DCREATE](d3dcreate.md) que controlan el comportamiento global del dispositivo. Estas constantes reflejan las constantes pasadas a [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) cuando se creó el dispositivo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetCreationParameters**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getcreationparameters)
</dt> <dt>

[**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> </dl>

 

 
