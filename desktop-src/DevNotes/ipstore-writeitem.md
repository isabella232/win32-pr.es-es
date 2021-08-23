---
description: Escribe un elemento de datos en el almacenamiento protegido.
ms.assetid: d940470c-b881-4e05-8e52-f804eac11e45
title: Método IPStore::WriteItem (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.WriteItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: d8af896d2aca8ae218ba06f94cb0e2ef5f86fc4122acf3463356f5fea3dafd1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955894"
---
# <a name="ipstorewriteitem-method"></a>Método IPStore::WriteItem

\[Protected Storage (Pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede que no esté disponible en versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura que proporcionan las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Escribe un elemento de datos en el almacenamiento protegido.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WriteItem(
  [in]        PST_KEY        Key,
  [in]  const GUID           *pItemType,
  [in]  const GUID           *pItemSubtype,
  [in]        LPCWSTR        *szItemName,
  [out]       DWORD          *cbData,
  [out]       BYTE           ppbData,
  [in]        PPST_PROMPTIFO pProomptInfo,
  [in]        DWORD          dwDefaultConfirmationStyle,
  [in]        DWORD          dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Clave* \[ En\]
</dt> <dd>

Área de almacenamiento del proveedor.



| Valor                                                                                                                                                                                                                                                   | Significado                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <dt>**PST \_ Clave \_ de \_ usuario actual**</dt> <dt>0x00000000</dt> </dl>    | El almacenamiento se mantiene en la sección de usuario actual del Registro.<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**PST \_ CLAVE \_ LOCAL \_ MACHINE**</dt> <dt>0x00000001</dt> </dl> | El almacenamiento se mantiene en la sección máquina local del registro.<br/> |



 

</dd> <dt>

*pItemType* \[ En\]
</dt> <dd>

Puntero a un **GUID que** identifica el tipo de datos del elemento de datos que se va a escribir.

</dd> <dt>

*pItemSubtype* \[ En\]
</dt> <dd>

Puntero a un **GUID que** identifica el subtipo de datos del elemento de datos que se va a escribir.

</dd> <dt>

*szItemName* \[ En\]
</dt> <dd>

Puntero a una cadena que contiene el nombre asignado al elemento de datos almacenado.

</dd> <dt>

*cbData* \[ out\]
</dt> <dd>

Puntero a un **DWORD** que indica el tamaño del búfer que contiene el elemento de datos almacenado.

</dd> <dt>

*ppbData* \[ out\]
</dt> <dd>

Puntero a un búfer que contiene el elemento de datos que se va a escribir.

</dd> <dt>

*pProomptInfo* \[ En\]
</dt> <dd>

Puntero a una [**estructura \_ PROMPTINFO de PST.**](pst-promptinfo.md)

</dd> <dt>

*dwDefaultConfirmationStyle* \[ En\]
</dt> <dd>

Estilo de confirmación predeterminado.



| Value                                                                                                                                                                                                                             | Significado                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="PST_CF_DEFAULT"></span><span id="pst_cf_default"></span><dl> <dt>**PST \_ CF \_ DEFAULT**</dt> <dt>0x00000000</dt> </dl> | Permite al usuario elegir el estilo de confirmación. <br/> |
| <span id="PST_CF_NONE"></span><span id="pst_cf_none"></span><dl> <dt>**PST \_ CF \_ NONE**</dt> <dt>0x00000001</dt> </dl>          | Fuerza la creación de elementos silenciosos. <br/>                      |



 

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

La interfaz de usuario y los comportamientos de seguridad de la operación de escritura.



| Value                                                                                                                                                                                                                                                              | Significado                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="PST_NO_OVERWRITE"></span><span id="pst_no_overwrite"></span><dl> <dt>**PST \_ NO \_ OVERWRITE**</dt> <dt>0x00000002</dt> </dl>                            | Especifica que el elemento se cree en el almacenamiento protegido. No se puede sobrescribir un elemento existente.<br/> |
| <span id="PST_UNRESTRICTED_ITEMDATA"></span><span id="pst_unrestricted_itemdata"></span><dl> <dt>**PST \_ ITEMDATA \_ sin**</dt> <dt>restricciones 0x00000004</dt> </dl> | Especifica que el flujo de datos no es seguro. De forma predeterminada, las llamadas a elementos son seguras.<br/>                         |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es un **valor HRESULT.** Un valor de **PST \_ E OK \_ indica** que la función se ha realizado correctamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| Archivo DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> <dt>

[**PROMPTINFO \_ de PST**](pst-promptinfo.md)
</dt> </dl>

 

 
