---
description: Deshabilita las características de.
ms.assetid: 2ea2dcfb-84e6-4f83-9afd-c3050b53f37c
title: pSetupSetGlobalFlags función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupSetGlobalFlags
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 6fcb56f26d5aea233156e0fe3dfab13099d29df7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650132"
---
# <a name="psetupsetglobalflags-function"></a>pSetupSetGlobalFlags función)

\[Esta función no está disponible en Windows Vista ni Windows Server 2008.\]

Deshabilita las características de.

## <a name="syntax"></a>Sintaxis


```C++
VOID pSetupSetGlobalFlags(
  _In_ DWORD Value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Valor* \[ de de\]
</dt> <dd>

Marcas usadas para deshabilitar la interfaz de usuario o la copia de seguridad automática.



| Value                                                                                                                                                                                                                                         | Significado                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="PSPGF_NONINTERACTIVE"></span><span id="pspgf_noninteractive"></span><dl> <dt>**PSPGF \_**</dt> <dt>0x004</dt> no interactivo </dl> | Establezca en deshabilitar la interfaz de usuario.<br/>   |
| <span id="PSPGF_NO_BACKUP"></span><span id="pspgf_no_backup"></span><dl> <dt>**PSPGF \_ SIN \_**</dt> <dt>0x002</dt> de copia de seguridad </dl>               | Establezca esta configuración en deshabilitar copia de seguridad automática.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
