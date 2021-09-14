---
description: Define los tipos de dispositivo.
ms.assetid: 2bcdc476-7c42-4152-b107-58366faf2abd
title: Enumeración D3DDEVTYPE (D3D9Types.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242865"
---
# <a name="d3ddevtype-enumeration"></a>D3DDEVTYPE (enumeración)

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

<span id="D3DDEVTYPE_HAL"></span><span id="d3ddevtype_hal"></span>**D3DDEVTYPE \_ HAN**
</dt> <dd>

Rasterización de hardware. El sombreado se realiza con software, hardware o transformación e iluminación mixtas.

</dd> <dt>

<span id="D3DDEVTYPE_NULLREF"></span><span id="d3ddevtype_nullref"></span>**D3DDEVTYPE \_ NULLREF**
</dt> <dd>

Inicialice Direct3D en un equipo que no tenga disponible el hardware ni la rasterización de referencia, y habilite los recursos para la creación de contenido 3D. Vea la sección Comentarios.

</dd> <dt>

<span id="D3DDEVTYPE_REF"></span><span id="d3ddevtype_ref"></span>**D3DDEVTYPE \_ REF**
</dt> <dd>

Las características de Direct3D se implementan en software; sin embargo, el rasterizador de referencia hace uso de instrucciones especiales de CPU siempre que puede.

El dispositivo de referencia se instala mediante Windows SDK 8.0 o posterior y está pensado como ayuda para la depuración solo para el desarrollo.

</dd> <dt>

<span id="D3DDEVTYPE_SW"></span><span id="d3ddevtype_sw"></span>**D3DDEVTYPE \_ SW**
</dt> <dd>

Un dispositivo de software conectable que se ha registrado con [**IDirect3D9::RegisterSoftwareDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-registersoftwaredevice).

</dd> <dt>

<span id="D3DDEVTYPE_FORCE_DWORD"></span><span id="d3ddevtype_force_dword"></span>**D3DDEVTYPE \_ FORCE \_ DWORD**
</dt> <dd>

Fuerza esta enumeración a compilar hasta 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilase a un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Todos los métodos de [**la interfaz IDirect3D9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3d9) que toman un tipo de dispositivo **D3DDEVTYPE** producirán un error si se especifica D3DDEVTYPE \_ NULLREF. Para usar estos métodos, sustituya D3DDEVTYPE \_ REF en la llamada al método .

Se debe crear un dispositivo D3DDEVTYPE REF en la memoria SCRATCH de D3DPOOL, a menos que se requieran búferes de \_ \_ vértices e índices. Para admitir búferes de vértices e índices, cree el dispositivo en la memoria SYSTEMMEM de D3DPOOL. \_

Si D3dref9.dll está instalado, Direct3D usará el rasterizador de referencia para crear un tipo de dispositivo D3DDEVTYPE REF, incluso si se especifica \_ D3DDEVTYPE \_ NULLREF. Si D3dref9.dll no está disponible y se especifica D3DDEVTYPE NULLREF, Direct3D no representará \_ ni presentará la escena.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



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

[**PARÁMETROS DE CREACIÓN DE DISPOSITIVOS D3D \_ \_**](d3ddevice-creation-parameters.md)
</dt> </dl>

 

 
