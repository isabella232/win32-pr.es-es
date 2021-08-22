---
title: Método AddMapping de IDWriteFontFallbackBuilder
description: Anexa una asignación única a la lista. Llame a esto una vez para cada asignación adicional.
ms.assetid: FCA3CD9C-9FB3-49BD-B4D1-53AEAAAAEE8A
keywords:
- Escritura directa del método AddMapping
- Método AddMapping Direct Write , interfaz IDWriteFontFallbackBuilder
- IdWriteFontFallbackBuilder interface Direct Write , AddMapping (método)
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
ms.openlocfilehash: 0b6496ac9ef9bdfa574cc2c4710ed4620fd855dbf5eff2b22885b32bf343d141
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650445"
---
# <a name="idwritefontfallbackbuilderaddmapping-method"></a>Método IDWriteFontFallbackBuilder::AddMapping

Anexa una asignación única a la lista. Llame a esto una vez para cada asignación adicional.

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

*fontCollection* \[ in, opcional\]
</dt> <dd>

Tipo: **[ **IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)**

Colección de fuentes explícita opcional para esta asignación.

</dd> <dt>

*localeName* \[ in, opcional\]
</dt> <dd>

Tipo: **const \* WCHAR**

Configuración regional del contexto.

</dd> <dt>

*baseFamilyName* \[ in, opcional\]
</dt> <dd>

Tipo: **const \* WCHAR**

Nombre de familia base con el que se debe coincidir, si procede.

</dd> <dt>

*scale* 
</dt> <dd>

Tipo: **FLOAT**

Factor de escala por el que se multiplica la fuente de destino del resultado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Server 2012 Aplicaciones de \[ escritorio R2 \| aplicaciones para UWP\]<br/>                          |
| Teléfono mínimo compatible<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 y Windows Runtime\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteFontFallbackBuilder**](idwritefontfallbackbuilder.md)
</dt> </dl>

 

