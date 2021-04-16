---
description: Lee el elemento de datos especificado del almacenamiento protegido.
ms.assetid: e565a0ea-5d8e-4706-a176-2305a95f0d67
title: 'IPStore:: ReadItem (método) (pstore. h)'
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
ms.openlocfilehash: 0464ef06bc7c2842d0c8f9ff76e8174f05338919
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671466"
---
# <a name="ipstorereaditem-method"></a>IPStore:: ReadItem (método)

\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

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

*Clave* \[ de de\]
</dt> <dd>

Área de almacenamiento del proveedor.



| Value                                                                                                                                                                                                                                                   | Significado                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <dt>**Archivo pst \_ \_ \_ Usuario actual clave**</dt> <dt>0x00000000</dt> </dl>    | El almacenamiento se mantiene en la sección usuario actual del registro.<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**Archivo pst \_ \_ \_ Máquina local de claves**</dt> <dt>0x00000001</dt> </dl> | El almacenamiento se mantiene en la sección del equipo local del registro.<br/> |



 

</dd> <dt>

*pItemType* \[ de\]
</dt> <dd>

Un puntero a un GUID que identifica el tipo de datos del elemento que se va a leer.

</dd> <dt>

*pItemSubtype* \[ de\]
</dt> <dd>

Un puntero a un GUID que identifica el subtipo de datos del elemento que se va a leer.

</dd> <dt>

*szItemName* \[ de\]
</dt> <dd>

Puntero a una cadena que contiene el nombre asignado al elemento de datos almacenado.

</dd> <dt>

*cbData* \[ de\]
</dt> <dd>

**DWORD** que indica el tamaño del búfer que contiene el elemento de datos almacenado.

</dd> <dt>

*pbData* \[ de\]
</dt> <dd>

Puntero a un búfer que contiene el elemento de datos almacenado.

</dd> <dt>

*pPromptInfo* \[ de\]
</dt> <dd>

Puntero a una estructura [**\_ PROMPTINFO de PST**](pst-promptinfo.md) .

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Especifica la interfaz de usuario y los comportamientos de seguridad para la operación de lectura.

Los valores de marca se pueden combinar con un operador lógico OR.



| Value                                                                                                                                                                                                                                                              | Significado                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PST_UNRESTRICTED_ITEMDATA"></span><span id="pst_unrestricted_itemdata"></span><dl> <dt>**Archivo pst \_ No RESTRINGIdo de \_ ITEMDATA**</dt> <dt>0x00000004</dt> </dl> | Especifica que el flujo de datos no es seguro. De forma predeterminada, las llamadas a elementos son seguras.<br/>                                                                                                                                             |
| <span id="PST_PROMPT_QUERY"></span><span id="pst_prompt_query"></span><dl> <dt>**Archivo pst \_ SOLICITAR \_ consulta**</dt> <dt>0x00000008</dt> </dl>                            | Especifica que la confirmación se devolverá cuando se realice correctamente. Si la interfaz de usuario está habilitada, se devuelve una operación correcta de **PST \_ E \_ Aceptar** . Si la interfaz de usuario no está habilitada, se devuelve un valor de **\_ \_ elemento \_ PST E** .<br/> |
| <span id="PST_NO_UI_MIGRATION"></span><span id="pst_no_ui_migration"></span><dl> <dt>**Archivo pst \_ SIN \_ \_ migración de IU**</dt> <dt>0x00000010</dt> </dl>                  | No mostrar la interfaz de usuario a menos que se requiera una contraseña personalizada.<br/>                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es un valor **HRESULT** . Un valor de **PST \_ E \_ OK** indica que la función se realizó correctamente.

## <a name="remarks"></a>Observaciones

Si **ReadItem** se completa correctamente, la aplicación es responsable de liberar el búfer de datos devuelto mediante la función [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| Archivo DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> <dt>

[**PST \_ PROMPTINFO**](pst-promptinfo.md)
</dt> </dl>

 

 
