---
description: Agrega un nombre de red local alternativo para el equipo desde el que se llama.
ms.assetid: e4d8355b-0492-4b6f-988f-3887e63a2bba
title: Función AddLocalAlternateComputerName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddLocalAlternateComputerName
- AddLocalAlternateComputerNameA
- AddLocalAlternateComputerNameW
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
- kernel32legacy.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
- API-Ms-Win-Core-Kernel32-Legacy-Ansi-L1-1-0.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
ms.openlocfilehash: 90945188209abdcaf16a7250e43db2af9a99ab4a3fbb55b8baabf0ea610c99e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118668687"
---
# <a name="addlocalalternatecomputername-function"></a>Función AddLocalAlternateComputerName

Agrega un nombre de red local alternativo para el equipo desde el que se llama.

## <a name="syntax"></a>Sintaxis


```C++
DWORD AddLocalAlternateComputerName(
  _In_ LPCTSTR lpDnsFQHostname,
  _In_ ULONG   ulFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpDnsFQHostname* \[ En\]
</dt> <dd>

Nombre alternativo que se va a agregar. El nombre debe tener el formato **ComputerNameDnsFullyQualified** tal como se define en la enumeración [**COMPUTER NAME \_ \_ FORMAT**](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format) y la función [**DnsValidateName \_ W**](/windows/win32/api/windns/nf-windns-dnsvalidatename) debe poder validarlo con su formato establecido en **DnsNameHostnameFull**.

</dd> <dt>

*ulFlags* \[ En\]
</dt> <dd>

Este parámetro está reservado y debe establecerse en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, la función devuelve **ERROR \_ SUCCESS**. Si se produce un error en la función, devuelve un código de error distinto de cero. Entre los códigos de error que devuelve se encuentran los siguientes:



| Código devuelto                                                                                               | Descripción                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERROR \_ PARÁMETRO NO \_ VÁLIDO**</dt> </dl>  | Indica que el parámetro *lpDnsFQHostname* no apunta a un nombre DNS válido o que el parámetro *ulFlags* no es igual a cero.<br/> |
| <dl> <dt>**ERROR \_ NO HAY SUFICIENTE \_ \_ MEMORIA**</dt> </dl> | no hay suficiente memoria para completar la operación.<br/>                                                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-----------------------------------|-------------------------------------------------------------------------------------------------------|
| Biblioteca<br/>                | <dl> <dt>Kernel32.lib</dt> </dl>               |
| Archivo DLL<br/>                    | <dl> <dt>Kernel32.dll</dt> </dl>               |
| Nombres Unicode y ANSI<br/> | **AddLocalAlternateComputerNameW** (Unicode) y **AddLocalAlternateComputerNameA** (ANSI)<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FORMATO DE \_ NOMBRE \_ DE EQUIPO**](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format)
</dt> <dt>

[**DnsValidateName \_ W**](/windows/win32/api/windns/nf-windns-dnsvalidatename)
</dt> </dl>

 

 
