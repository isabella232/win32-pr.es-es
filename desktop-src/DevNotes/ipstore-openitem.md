---
description: Abre un elemento para varios accesos.
ms.assetid: b0602abd-dbda-40d0-befa-348c1179fa4f
title: Método IPStore::OpenItem (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.OpenItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 8817930f19e519083df083ac3a6d81bd5c48f8f649847c5ef9f86d3ff4cee9d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118004215"
---
# <a name="ipstoreopenitem-method"></a>Método IPStore::OpenItem

\[Protected Storage (Pstore) está disponible para su uso en Windows Server 2003 y Windows XP. Solo está disponible para operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede que no esté disponible en versiones posteriores. Pstore usa una implementación anterior de la protección de datos. Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura que proporcionan las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Abre un elemento para varios accesos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OpenItem(
  [in]       PST_KEY        Key,
  [in] const PSGUID         *pItemType,
  [in] const GUID           *pItemSubtype,
  [in]       LPCWSTR        *szItemName,
  [in]       PST_ACCESSMODE ModeFlags,
  [in]       PPST_PROMPTIFO pProomptInfo,
  [in]       DWORD          dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Clave* \[ En\]
</dt> <dd>

Especifica si el tipo es local para el equipo o solo está asociado al usuario que crea.



| Valor                                                                                                                                                                                                                                                   | Significado                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <dt>**PST \_ Clave \_ actual \_ del usuario**</dt> <dt>0x00000000</dt> </dl>    | El almacenamiento se mantiene en la sección de usuario actual del registro.<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**PST \_ Clave \_ de \_ máquina local**</dt> <dt>0x00000001</dt> </dl> | El almacenamiento se mantiene en la sección máquina local del registro.<br/> |



 

</dd> <dt>

*pItemType* \[ En\]
</dt> <dd>

Puntero a un GUID que identifica el tipo de datos del elemento que se debe abrir.

</dd> <dt>

*pItemSubtype* \[ En\]
</dt> <dd>

Puntero a un GUID que indica el subtipo de elemento que se abrirá.

</dd> <dt>

*szItemName* \[ En\]
</dt> <dd>

Cadena que contiene el nombre del elemento que se abrirá.

</dd> <dt>

*ModeFlags* \[ En\]
</dt> <dd>

Describe los modos de acceso a los que pertenece un conjunto especificado de cláusulas de acceso. Para obtener más información, vea [**PStore Types**](pstore-types.md).



| Value                                                                                                                                                                                                         | Significado                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="PST_READ"></span><span id="pst_read"></span><dl> <dt>**PST \_ Lectura**</dt> <dt>0x0001</dt> </dl>    | Modo de acceso de lectura.<br/>  |
| <span id="PST_WRITE"></span><span id="pst_write"></span><dl> <dt>**PST \_ Escritura**</dt> <dt>0x0002</dt> </dl> | Modo de acceso de escritura.<br/> |



 

</dd> <dt>

*pProomptInfo* \[ En\]
</dt> <dd>

Puntero a una [**estructura \_ PROMPTINFO de PST.**](pst-promptinfo.md)

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Reservado: debe establecerse en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **un valor HRESULT.** Un valor de **PST \_ E OK \_ indica** que la función se ha realizado correctamente.

## <a name="remarks"></a>Comentarios

El **uso de OpenItem** para abrir un elemento en la base de datos de almacenamiento protegida requiere que finalmente se cierre mediante [**IPStore::CloseItem**](ipstore-closeitem.md) para evitar una pérdida de memoria.

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

 

 
