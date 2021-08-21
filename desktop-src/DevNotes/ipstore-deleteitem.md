---
description: Elimina el elemento especificado del almacenamiento protegido.
ms.assetid: 1d071245-a563-4fba-9300-c47ca9a9d625
title: Método IPStore::D eleteItem (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.DeleteItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: e99a2ec9b39b035b4a4af24aa18c2936decd399043cc507ed0bf279c5696fd53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667456"
---
# <a name="ipstoredeleteitem-method"></a>Método IPStore::D eleteItem

\[Protected Storage (Pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede que no esté disponible en versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura que proporcionan las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Elimina el elemento especificado del almacenamiento protegido.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DeleteItem(
  [in]       PST_KEY         Key,
  [in] const GUID            *pItemType,
  [in] const GUID            *pItemSubType,
  [in]       LPCWSTR         szItemName,
  [in]       PPST_PROMPTINFO pPromptInfo,
  [in]       DWORD           dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Clave* \[ En\]
</dt> <dd>

Área de almacenamiento del proveedor.



| Value                                                                                                                                                                                                                                                   | Significado                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <dt>**PST \_ Clave \_ de \_ usuario actual**</dt> <dt>0x00000000</dt> </dl>    | El almacenamiento se mantiene en la sección de usuario actual del registro.<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**PST \_ Clave \_ de \_ máquina local**</dt> <dt>0x00000001</dt> </dl> | El almacenamiento se mantiene en la sección máquina local del registro.<br/> |



 

</dd> <dt>

*pItemType* \[ En\]
</dt> <dd>

Puntero a un **GUID** que identifica el tipo de datos del elemento que se eliminará.

</dd> <dt>

*pItemSubType* \[ En\]
</dt> <dd>

GUID **que** indica el subtipo de elemento que se debe eliminar.

</dd> <dt>

*szItemName* \[ En\]
</dt> <dd>

Cadena que contiene el nombre del elemento que se eliminará.

</dd> <dt>

*pPromptInfo* \[ En\]
</dt> <dd>

Puntero a una [**estructura \_ PROMPTINFO de PST.**](pst-promptinfo.md)

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Especifica los comportamientos de seguridad y la interfaz de usuario para la operación de eliminación.



| Value                                                                                                                                                                                                                                             | Significado                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="PST_NO_UI_MIGRATION"></span><span id="pst_no_ui_migration"></span><dl> <dt>**PST \_ NO SE \_ HA \_ 0X00000010**</dt> <dt></dt> </dl> | No muestre la interfaz de usuario a menos que se requiera una contraseña personalizada.<br/> |



 

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

 

 
