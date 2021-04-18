---
description: 'El tipo de datos de identificador de la \_ enumeración LSA \_ lo usa la función LSA que enumera los objetos TrustedDomain: LsaEnumerateTrustedDomainsEx.'
ms.assetid: 99dad3aa-cb92-4b7e-8a18-2c977cb2737c
title: LSA_ENUMERATION_HANDLE (Ntsecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db71e9522a188956a7aa838b11ba74f08bde39c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687574"
---
# <a name="lsa_enumeration_handle"></a>\_identificador de enumeración de LSA \_

El tipo de datos de identificador de la **\_ enumeración \_ LSA** lo usa la función LSA que enumera los objetos [**TrustedDomain**](trusteddomain-object.md) : [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex). Esta función está diseñada para que pueda realizar varias llamadas para enumerar todos los objetos de un tipo determinado en la base de datos.

En la llamada de función de enumeración inicial, se pasa un puntero a una variable de **\_ \_ identificador de enumeración de LSA** que se inicializa en cero. La función actualiza este valor. Si la función devuelve un valor que indica que hay más objetos para enumerar, llame de nuevo a la función y pase el valor de identificador de la **\_ \_ enumeración LSA** actualizado para obtener una enumeración que continúe desde el punto en el que se quedó la enumeración anterior.


```C++
typedef ULONG LSA_ENUMERATION_HANDLE, *PLSA_ENUMERATION_HANDLE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Ntsecapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex)
</dt> </dl>

 

 




