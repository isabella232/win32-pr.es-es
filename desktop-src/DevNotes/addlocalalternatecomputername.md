---
description: Agrega un nombre de red local alternativo para el equipo desde el que se llama.
ms.assetid: e4d8355b-0492-4b6f-988f-3887e63a2bba
title: AddLocalAlternateComputerName función)
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
ms.openlocfilehash: 6027752a0e60f135f0cc8a1c0cdd536c59c09621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650011"
---
# <a name="addlocalalternatecomputername-function"></a>AddLocalAlternateComputerName función)

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

*lpDnsFQHostname* \[ de\]
</dt> <dd>

Nombre alternativo que se va a agregar. El nombre debe estar en el formato **ComputerNameDnsFullyQualified** , tal y como se define en la enumeración de [**\_ \_ formato de nombre de equipo**](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format) , y la función [**DnsValidateName \_ W**](/windows/win32/api/windns/nf-windns-dnsvalidatename) debe ser capaz de validarla con su formato establecido en **DnsNameHostnameFull**.

</dd> <dt>

*ulFlags* \[ de\]
</dt> <dd>

Este parámetro está reservado y debe establecerse en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, la función devuelve el **error \_ Success**. Si se produce un error en la función, devuelve un código de error distinto de cero. Entre los códigos de error que devuelve se encuentran los siguientes:



| Código devuelto                                                                                               | Descripción                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERROR \_ de \_ parámetro no válido**</dt> </dl>  | Indica que el parámetro *lpDnsFQHostname* no apunta a un nombre DNS válido o que el parámetro *ulFlags* no es igual a cero.<br/> |
| <dl> <dt>**ERROR \_ de \_ memoria insuficiente \_**</dt> </dl> | no hay suficiente memoria para completar la operación.<br/>                                                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-----------------------------------|-------------------------------------------------------------------------------------------------------|
| Biblioteca<br/>                | <dl> <dt>Kernel32.lib</dt> </dl>               |
| Archivo DLL<br/>                    | <dl> <dt>Kernel32.dll</dt> </dl>               |
| Nombres Unicode y ANSI<br/> | **AddLocalAlternateComputerNameW** (Unicode) y **AddLocalAlternateComputerNameA** (ANSI)<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_formato de nombre de equipo \_**](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format)
</dt> <dt>

[**DnsValidateName \_ W**](/windows/win32/api/windns/nf-windns-dnsvalidatename)
</dt> </dl>

 

 
