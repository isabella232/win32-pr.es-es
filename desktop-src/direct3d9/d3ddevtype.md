---
description: Define los tipos de dispositivo.
ms.assetid: 2bcdc476-7c42-4152-b107-58366faf2abd
title: Enumeración D3DDEVTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 2be365ffbbe5bf778379c7be060c85c0b099422f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698212"
---
# <a name="d3ddevtype-enumeration"></a>Enumeración D3DDEVTYPE

Define los tipos de dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum D3DDEVTYPE { 
  D3DDEVTYPE_HAL          = 1,
  D3DDEVTYPE_NULLREF      = 4,
  D3DDEVTYPE_REF          = 2,
  D3DDEVTYPE_SW           = 3,
  D3DDEVTYPE_FORCE_DWORD  = 0xffffffff
} D3DDEVTYPE, *LPD3DDEVTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DDEVTYPE_HAL"></span><span id="d3ddevtype_hal"></span>**\_Hal D3DDEVTYPE**
</dt> <dd>

Rasterización de hardware. El sombreado se realiza con el software, el hardware o la transformación y la iluminación mixtas.

</dd> <dt>

<span id="D3DDEVTYPE_NULLREF"></span><span id="d3ddevtype_nullref"></span>**D3DDEVTYPE \_ NULLREF**
</dt> <dd>

Inicialice Direct3D en un equipo que no tenga hardware ni rasterización de referencia disponible y habilite los recursos para la creación de contenido 3D. Vea la sección Comentarios.

</dd> <dt>

<span id="D3DDEVTYPE_REF"></span><span id="d3ddevtype_ref"></span>**Referencia de D3DDEVTYPE \_**
</dt> <dd>

Las características de Direct3D se implementan en el software; sin embargo, el rasterizador de referencia hace uso de instrucciones de CPU especiales siempre que sea posible.

El dispositivo de referencia se instala con el Windows SDK 8,0 o posterior y está pensado como ayuda para la depuración solo para el desarrollo.

</dd> <dt>

<span id="D3DDEVTYPE_SW"></span><span id="d3ddevtype_sw"></span>**D3DDEVTYPE \_ SW**
</dt> <dd>

Un dispositivo de software acoplable que se ha registrado con [**IDirect3D9:: RegisterSoftwareDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-registersoftwaredevice).

</dd> <dt>

<span id="D3DDEVTYPE_FORCE_DWORD"></span><span id="d3ddevtype_force_dword"></span>**D3DDEVTYPE \_ forzar \_ DWORD**
</dt> <dd>

Obliga a esta enumeración a compilarse en 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Se producirá un error en todos los métodos de la interfaz [**IDirect3D9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3d9) que toman un tipo de dispositivo **D3DDEVTYPE** si \_ se especifica D3DDEVTYPE NULLREF. Para usar estos métodos, sustituya D3DDEVTYPE \_ ref en la llamada al método.

Se \_ debe crear un dispositivo de referencia D3DDEVTYPE en la \_ memoria temporal de D3DPOOL, a menos que se requieran búferes de vértices y de índices. Para admitir los búferes de vértices y de índices, cree el dispositivo en D3DPOOL \_ SYSTEMMEM Memory.

Si D3dref9.dll está instalado, Direct3D usará el rasterizador de referencia para crear un \_ tipo de dispositivo D3DDEVTYPE Ref, incluso si \_ se especifica D3DDEVTYPE NULLREF. Si D3dref9.dll no está disponible y \_ se especifica D3DDEVTYPE NULLREF, Direct3D no representará ni presentará la escena.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)
</dt> <dt>

[**IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)
</dt> <dt>

[**IDirect3D9::CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)
</dt> <dt>

[**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> <dt>

[**IDirect3D9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps)
</dt> <dt>

[**\_Parámetros de creación de D3DDEVICE \_**](d3ddevice-creation-parameters.md)
</dt> </dl>

 

 
