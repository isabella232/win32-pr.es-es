---
description: Lee el elemento de datos especificado del almacenamiento protegido.
ms.assetid: e565a0ea-5d8e-4706-a176-2305a95f0d67
title: Método IPStore::ReadItem (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.ReadItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 516eb55772e375d09d3b134dee456c090cf11d6ef0d10905f99a822b1df0d9e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001495"
---
# <a name="ipstorereaditem-method"></a>Método IPStore::ReadItem

\[Protected Storage (Pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede que no esté disponible en versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura que proporcionan las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Lee el elemento de datos especificado del almacenamiento protegido.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ReadItem(
  [in]       PST_KEY        Key,
  [in] const PSGUID         *pItemType,
  [in] const GUID           *pItemSubtype,
  [in]       LPCWSTR        *szItemName,
  [in]       DWORD          cbData,
  [in]       BYTE_RPC_FAR   *pbData,
  [in]       PPST_PROMPTIFO pPromptInfo,
  [in]       DWORD          dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Clave* \[ En\]
</dt> <dd>

Área de almacenamiento del proveedor.



| Value                                                                                                                                                                                                                                                   | Significado                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <dt>**PST \_ Clave \_ de \_ usuario actual**</dt> <dt>0x00000000</dt> </dl>    | El almacenamiento se mantiene en la sección de usuario actual del Registro.<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**PST \_ CLAVE \_ LOCAL \_ MACHINE**</dt> <dt>0x00000001</dt> </dl> | El almacenamiento se mantiene en la sección máquina local del registro.<br/> |



 

</dd> <dt>

*pItemType* \[ En\]
</dt> <dd>

Puntero a un GUID que identifica el tipo de datos del elemento que se debe leer.

</dd> <dt>

*pItemSubtype* \[ En\]
</dt> <dd>

Puntero a un GUID que identifica el subtipo de datos del elemento que se debe leer.

</dd> <dt>

*szItemName* \[ En\]
</dt> <dd>

Puntero a una cadena que contiene el nombre asignado al elemento de datos almacenado.

</dd> <dt>

*cbData* \[ En\]
</dt> <dd>

DWORD **que** indica el tamaño del búfer que contiene el elemento de datos almacenado.

</dd> <dt>

*pbData* \[ En\]
</dt> <dd>

Puntero a un búfer que contiene el elemento de datos almacenado.

</dd> <dt>

*pPromptInfo* \[ En\]
</dt> <dd>

Puntero a una [**estructura \_ PROMPTINFO de PST.**](pst-promptinfo.md)

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Especifica los comportamientos de seguridad y la interfaz de usuario para la operación de lectura.

Los valores de marca se pueden combinar con un or lógico.



| Value                                                                                                                                                                                                                                                              | Significado                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PST_UNRESTRICTED_ITEMDATA"></span><span id="pst_unrestricted_itemdata"></span><dl> <dt>**PST \_ ITEMDATA \_ sin**</dt> <dt>restricciones 0x00000004</dt> </dl> | Especifica que el flujo de datos no es seguro. De forma predeterminada, las llamadas a elementos son seguras.<br/>                                                                                                                                             |
| <span id="PST_PROMPT_QUERY"></span><span id="pst_prompt_query"></span><dl> <dt>**PST \_ Solicitud \_ de consulta**</dt> <dt>0x00000008</dt> </dl>                            | Especifica que la confirmación se devuelva cuando se haya hecho correctamente. Si la interfaz de usuario está habilitada, se devuelve **un valor correcto de PST E \_ \_ OK.** Si la interfaz de usuario no está habilitada, se devuelve un valor de **PST \_ E ITEM \_ \_ EXISTS.**<br/> |
| <span id="PST_NO_UI_MIGRATION"></span><span id="pst_no_ui_migration"></span><dl> <dt>**PST \_ NO SE \_ HA \_ 0X00000010**</dt> <dt></dt> </dl>                  | No muestre la interfaz de usuario a menos que se requiera una contraseña personalizada.<br/>                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es un **valor HRESULT.** Un valor de **PST \_ E OK \_ indica** que la función se ha realizado correctamente.

## <a name="remarks"></a>Comentarios

Si **ReadItem** se completa correctamente, la aplicación es responsable de liberar el búfer de datos devuelto mediante la [**función CoTaskMemFree.**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)

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

 

 
