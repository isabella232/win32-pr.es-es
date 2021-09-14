---
title: Método AddMapping de IDWriteFontFallbackBuilder
description: Anexa una asignación única a la lista. Llámela una vez para cada asignación adicional.
ms.assetid: FCA3CD9C-9FB3-49BD-B4D1-53AEAAAAEE8A
keywords:
- Escritura directa del método AddMapping
- Método AddMapping Direct Write , interfaz IDWriteFontFallbackBuilder
- IdWriteFontFallbackBuilder interface Direct Write , AddMapping (Método AddMapping)
topic_type:
- apiref
api_name:
- IDWriteFontFallbackBuilder.AddMapping
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a084aa2a9df0e34741c8bf5f39ae00933d49cfe7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173750"
---
# <a name="idwritefontfallbackbuilderaddmapping-method"></a>Método IDWriteFontFallbackBuilder::AddMapping

Anexa una asignación única a la lista. Llámela una vez para cada asignación adicional.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AddMapping(
                       DWRITE_UNICODE_RANGE  *ranges,
                       UINT32                rangesCount,
  [in]           const WCHAR                 **targetFamilyNames,
                       UINT32                targetFamilyNamesCount,
  [in, optional]       IDWriteFontCollection fontCollection = nullptr,
  [in, optional] const WCHAR                 *localeName = nullptr,
  [in, optional] const WCHAR                 *baseFamilyName = nullptr,
                       FLOAT                 scale = 1
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Gamas* 
</dt> <dd>

Tipo: **[ **DWRITE \_ UNICODE \_ RANGE**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_unicode_range)\***

Intervalos Unicode que se aplican a esta asignación.

</dd> <dt>

*rangesCount* 
</dt> <dd>

Tipo: **UINT32**

Número de intervalos Unicode.

</dd> <dt>

*targetFamilyNames* \[ En\]
</dt> <dd>

Tipo: **const \* \* WCHAR**

Lista de cadenas de nombre de familia de destino.

</dd> <dt>

*targetFamilyNamesCount* 
</dt> <dd>

Tipo: **UINT32**

Número de nombres de familia de destino.

</dd> <dt>

*fontCollection* \[ en, opcional\]
</dt> <dd>

Tipo: **[ **IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)**

Colección de fuentes explícita opcional para esta asignación.

</dd> <dt>

*localeName* \[ en, opcional\]
</dt> <dd>

Tipo: **const \* WCHAR**

Configuración regional del contexto.

</dd> <dt>

*baseFamilyName* \[ en, opcional\]
</dt> <dd>

Tipo: **const \* WCHAR**

Nombre de familia base con el que se debe coincidir, si procede.

</dd> <dt>

*scale* 
</dt> <dd>

Tipo: **FLOAT**

Factor de escala por el que multiplicar la fuente de destino de resultado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Server 2012 Aplicaciones de \[ escritorio R2 \| para aplicaciones para UWP\]<br/>                          |
| Teléfono mínimo compatible<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 y Windows Runtime\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteFontFallbackBuilder**](idwritefontfallbackbuilder.md)
</dt> </dl>

 

