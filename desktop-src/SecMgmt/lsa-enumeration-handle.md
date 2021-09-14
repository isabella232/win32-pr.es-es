---
description: 'La función LSA usa el tipo de datos LSA ENUMERATION HANDLE que enumera objetos \_ \_ TrustedDomain: LsaEnumerateTrustedDomainsEx.'
ms.assetid: 99dad3aa-cb92-4b7e-8a18-2c977cb2737c
title: LSA_ENUMERATION_HANDLE (Ntsecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db71e9522a188956a7aa838b11ba74f08bde39c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374871"
---
# <a name="lsa_enumeration_handle"></a>IDENTIFICADOR DE ENUMERACIÓN LSA \_ \_

La función LSA usa el tipo de datos **LSA \_ ENUMERATION \_ HANDLE** que enumera objetos [**TrustedDomain:**](trusteddomain-object.md) [**LsaEnumerateTrustedDomainsEx.**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex) Esta función está diseñada para que pueda realizar varias llamadas para enumerar todos los objetos de un tipo determinado en la base de datos.

En la llamada de función de enumeración inicial, se pasa un puntero a una variable **LSA \_ ENUMERATION \_ HANDLE** que se inicializa en cero. La función actualiza este valor. Si la función devuelve un valor que indica que hay más objetos para enumerar, llame de nuevo a la función y pase el valor actualizado **LSA \_ ENUMERATION \_ HANDLE** para obtener una enumeración que continúe desde el punto en el que se dejó la enumeración anterior.


```C++
typedef ULONG LSA_ENUMERATION_HANDLE, *PLSA_ENUMERATION_HANDLE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Ntsecapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex)
</dt> </dl>

 

 




