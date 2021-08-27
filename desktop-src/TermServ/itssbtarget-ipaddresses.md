---
title: Propiedad ITsSbTarget IpAddresses
description: Recupera o especifica las direcciones IP externas del destino.
ms.assetid: 938a753c-d541-4772-b41b-817324488685
ms.tgt_platform: multiple
keywords:
- Propiedad TargetExternalIpAddresses Servicios de Escritorio remoto
- Propiedad TargetExternalIpAddresses Servicios de Escritorio remoto , interfaz ITsSbTarget
- Propiedad TargetExternalIpAddresses Servicios de Escritorio remoto , interfaz ITsSbTarget
- Propiedad IpAddresses Servicios de Escritorio remoto
- Propiedad IpAddresses Servicios de Escritorio remoto , interfaz ITsSbTarget
- Interfaz ITsSbTarget Servicios de Escritorio remoto , propiedad IpAddresses
- Propiedad IpAddresses Servicios de Escritorio remoto , interfaz ITsSbTargetEx
- Interfaz ITsSbTargetEx Servicios de Escritorio remoto , propiedad IpAddresses
topic_type:
- apiref
api_name:
- ITsSbTarget.IpAddresses
- ITsSbTarget.get_IpAddresses
- ITsSbTarget.put_IpAddresses
- ITsSbTargetEx.IpAddresses
- ITsSbTargetEx.get_IpAddresses
- ITsSbTargetEx.put_IpAddresses
- TargetExternalIpAddresses
- ITsSbTarget.TargetExternalIpAddresses
- ITsSbTarget get_TargetExternalIpAddresses
- ITsSbTarget put_TargetExternalIpAddresses
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21afd8d2349bfef37dcc39b684c3f5b837728f79
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988278"
---
# <a name="itssbtargetipaddresses-property"></a>Propiedad ITsSbTarget::IpAddresses

Recupera o especifica las direcciones IP externas del destino.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_IpAddresses(
  [in, size_is(numAddresses)]   TSSD_ConnectionPoint *sockaddr,
  [in]                          DWORD                numAddresses
);

HRESULT get_IpAddresses(
  [out, size_is(*numAddresses)] TSSD_ConnectionPoint *sockaddr,
  [in, out]                     DWORD                *numAddresses
);
```



## <a name="property-value"></a>Valor de propiedad

Puntero a una matriz de [**estructuras \_ connectionPoint de TSSD**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) que reciben las direcciones IP externas del destino.

Puntero a una variable **DWORD** que contiene el número de direcciones IP externas en *el parámetro sockaddr.* Si se desconoce el número de direcciones, pase *sockaddr* como **NULL.** El método devolverá el número de estructuras [**de \_ ConnectionPoint de TSSD**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) necesarias para asignar en la matriz a la que apunta *el parámetro sockaddr.*

## <a name="remarks"></a>Observaciones

Esta propiedad se conocía anteriormente como **TargetExternalIpAddresses** en Windows Server 2008 R2.

Si se desconoce el número de direcciones IP externas, puede llamar a este método con *sockaddr* establecido en **NULL.** A continuación, el método devolverá, en el parámetro *numAddresses,* el número de estructuras [**de \_ ConnectionPoint de TSSD**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) necesarias para recibir todas las direcciones IP externas. Asigne la matriz para *sockaddr* en función de este número y, a continuación, llame al método de nuevo, estableciendo *sockaddr* en la matriz recién asignada y *numAddresses* en el número devuelto por la primera llamada.

## <a name="requirements"></a>Requisitos




| Requisito | Value |
|--------|-------|
| Cliente mínimo compatible<br /> | No se admite ninguno<br /> | 
| Servidor mínimo compatible<br /> | Windows Server 2012<br /> | 
| IDL<br /> | <dl><dt>Sbtsv.idl</dt></dl> | 
| IID<br /> | IID_ITsSbTarget se define como:<ul><li>16616ECC-272D-411D-B324-126893033856</li><li>e85e10ea-db0b-4752-b456-5fd5840901c0 en Windows Server 2008 R2</li></ul> | 




## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dt>

[**Punto de conexión de TSSD \_**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint)
</dt> </dl>

 

 





