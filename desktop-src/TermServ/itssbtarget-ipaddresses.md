---
title: Propiedad IpAddresses de ITsSbTarget
description: Recupera o especifica las direcciones IP externas del destino.
ms.assetid: 938a753c-d541-4772-b41b-817324488685
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad TargetExternalIpAddresses
- Propiedad TargetExternalIpAddresses Servicios de Escritorio remoto, interfaz ITsSbTarget
- Propiedad TargetExternalIpAddresses Servicios de Escritorio remoto, interfaz ITsSbTarget
- Servicios de Escritorio remoto de la propiedad IpAddresses
- Propiedad IpAddresses Servicios de Escritorio remoto, interfaz ITsSbTarget
- Servicios de Escritorio remoto de la interfaz ITsSbTarget, propiedad IpAddresses
- Propiedad IpAddresses Servicios de Escritorio remoto, interfaz ITsSbTargetEx
- Servicios de Escritorio remoto de la interfaz ITsSbTargetEx, propiedad IpAddresses
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
ms.openlocfilehash: c8b3902840b24bc49ae3bda0510c8355afb67810
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419518"
---
# <a name="itssbtargetipaddresses-property"></a>ITsSbTarget:: IpAddresses (propiedad)

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

Un puntero a una matriz de [**estructuras \_ TSSD**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) de un conjunto de discos que reciben las direcciones IP externas del destino.

Un puntero a una variable **DWORD** que contiene el número de direcciones IP externas en el parámetro *sockaddr* . Si el número de direcciones es desconocido, pase *sockaddr* como **null**. El método devolverá el número de estructuras [**TSSD \_**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) de un valor necesario para asignar en la matriz señalada por el parámetro *sockaddr* .

## <a name="remarks"></a>Observaciones

Esta propiedad se conocía anteriormente como **TargetExternalIpAddresses** en Windows Server 2008 R2.

Si el número de direcciones IP externas es desconocido, puede llamar a este método con *sockaddr* establecido en **null**. Después, el método devolverá, en el parámetro *numAddresses* , el número de estructuras de [**TSSD \_**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) de un valor necesario para recibir todas las direcciones IP externas. Asigne la matriz para *sockaddr* basándose en este número y, a continuación, llame de nuevo al método, estableciendo *sockaddr* en la matriz recién asignada y *numAddresses* en el número devuelto por la primera llamada.

## <a name="requirements"></a>Requisitos



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Cliente mínimo compatible<br/></td>
<td>No se admite ninguno<br/></td>
</tr>
<tr class="even">
<td>Servidor mínimo compatible<br/></td>
<td>Windows Server 2012<br/></td>
</tr>
<tr class="odd">
<td>IDL<br/></td>
<td><dl> <dt>Sbtsv. idl</dt> </dl></td>
</tr>
<tr class="even">
<td>IID<br/></td>
<td>IID_ITsSbTarget se define como:
<ul>
<li>16616ECC-272D-411D-B324-126893033856</li>
<li>e85e10ea-db0b-4752-B456-5fd5840901c0 en Windows Server 2008 R2</li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dt>

[**TSSD \_**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint)
</dt> </dl>

 

 





