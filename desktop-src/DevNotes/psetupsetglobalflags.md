---
description: Deshabilita las características.
ms.assetid: 2ea2dcfb-84e6-4f83-9afd-c3050b53f37c
title: Función pSetupSetGlobalFlags
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
ms.openlocfilehash: d28bb948d351b2b9ad54c7e2bdc8c8cbfde83f6f4ade42a0f90440eca28bfc05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955704"
---
# <a name="psetupsetglobalflags-function"></a>Función pSetupSetGlobalFlags

\[Esta función no está disponible en Windows Vista ni Windows Server 2008.\]

Deshabilita las características.

## <a name="syntax"></a>Sintaxis


```C++
VOID pSetupSetGlobalFlags(
  _In_ DWORD Value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Valor* \[ En\]
</dt> <dd>

Marcas que se usan para deshabilitar la interfaz de usuario o la copia de seguridad automática.



| Valor                                                                                                                                                                                                                                         | Significado                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="PSPGF_NONINTERACTIVE"></span><span id="pspgf_noninteractive"></span><dl> <dt>**PSPGF \_ NonINTERACTIVE**</dt> <dt>0x004</dt> </dl> | Establezca esta opción para deshabilitar la interfaz de usuario.<br/>   |
| <span id="PSPGF_NO_BACKUP"></span><span id="pspgf_no_backup"></span><dl> <dt>**PSPGF \_ NO \_ BACKUP**</dt> <dt>0x002</dt> </dl>               | Establezca esta opción para deshabilitar la copia de seguridad automática.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
