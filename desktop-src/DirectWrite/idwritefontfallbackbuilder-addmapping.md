---
title: IDWriteFontFallbackBuilder AddMapping, método
description: Anexa una única asignación a la lista. Llame a este método una vez por cada asignación adicional.
ms.assetid: FCA3CD9C-9FB3-49BD-B4D1-53AEAAAAEE8A
keywords:
- Método AddMapping de escritura directa
- Método AddMapping de escritura directa, interfaz IDWriteFontFallbackBuilder
- Interfaz IDWriteFontFallbackBuilder Direct Write, método AddMapping
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422444"
---
# <a name="idwritefontfallbackbuilderaddmapping-method"></a>IDWriteFontFallbackBuilder:: AddMapping (método)

Anexa una única asignación a la lista. Llame a este método una vez por cada asignación adicional.

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

*alcance* 
</dt> <dd>

Tipo: **\* [**DWRITE \_ \_ intervalo Unicode**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_unicode_range)* _

Intervalos Unicode que se aplican a esta asignación.

</dd> <dt>

_rangesCount * 
</dt> <dd>

Tipo: **UINT32**

Número de intervalos Unicode.

</dd> <dt>

*targetFamilyNames* \[ de\]
</dt> <dd>

Tipo: **const WCHAR \* \***

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

Colección de fuentes explícitas opcional para esta asignación.

</dd> <dt>

*localeName* \[ en, opcional\]
</dt> <dd>

Tipo: **const WCHAR \** _

Configuración regional del contexto.

</dd> <dt>

_baseFamilyName * \[ en, opcional\]
</dt> <dd>

Tipo: **const WCHAR \** _

Nombre de familia base con el que coincidir, si procede.

</dd> <dt>

_scale * 
</dt> <dd>

Tipo: **float**

Factor de escala para multiplicar la fuente de destino del resultado por.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]<br/>                                     |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]<br/>                          |
| Teléfono mínimo compatible<br/>  | Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteFontFallbackBuilder**](idwritefontfallbackbuilder.md)
</dt> </dl>

 

