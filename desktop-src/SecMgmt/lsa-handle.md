---
description: Identificador del objeto de directiva local.
ms.assetid: f5878d27-558b-4ef1-9401-1277e740c61d
title: LSA_HANDLE (Ntsecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07bd71a14666dde7bb92e439159a55dd71706612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082705"
---
# <a name="lsa_handle"></a>identificador de LSA \_

El tipo de datos de **\_ identificador de LSA** es un identificador del objeto de [**Directiva**](policy-object.md) local.


```C++
typedef PVOID LSA_HANDLE, *PLSA_HANDLE;
```



## <a name="remarks"></a>Observaciones

Antes de poder usar la API de directiva local, la aplicación debe abrir un identificador de un objeto de [**Directiva**](policy-object.md) . Para ello, llame a [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy). Esta función devuelve un identificador que la aplicación puede especificar en las siguientes llamadas de función de directiva de LSA.

Cada controlador tiene un conjunto asociado de permisos que determinan las operaciones que puede realizar la aplicación en el objeto de [**Directiva**](policy-object.md) mediante el uso del identificador. La aplicación puede abrir más de un identificador para el objeto de **Directiva** a la vez. Cuando ya no se necesita un identificador, la aplicación debe cerrarlo llamando a [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Ntsecapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose)
</dt> <dt>

[**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy)
</dt> </dl>

 

