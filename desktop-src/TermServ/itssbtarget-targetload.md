---
title: Propiedad TargetLoad de ITsSbTarget
description: Recupera la carga relativa de un destino.
ms.assetid: 56618dcf-1319-4310-80ba-7ed71b8b02e8
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad TargetLoad
- Propiedad TargetLoad Servicios de Escritorio remoto, interfaz ITsSbTarget
- Servicios de Escritorio remoto de la interfaz ITsSbTarget, propiedad TargetLoad
- Propiedad TargetLoad Servicios de Escritorio remoto, interfaz ITsSbTargetEx
- Servicios de Escritorio remoto de la interfaz ITsSbTargetEx, propiedad TargetLoad
topic_type:
- apiref
api_name:
- ITsSbTarget.TargetLoad
- ITsSbTarget.get_TargetLoad
- ITsSbTargetEx.TargetLoad
- ITsSbTargetEx.get_TargetLoad
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddfc9be9805406ab76b166e2a34bc47a7f5e9ab5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784120"
---
# <a name="itssbtargettargetload-property"></a>ITsSbTarget:: TargetLoad (propiedad)

Recupera la carga relativa de un destino. Este valor se basa en el número de sesiones existentes y pendientes. De forma predeterminada, una sesión pendiente tiene el mismo valor que una sesión existente.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_TargetLoad(
  [out, retval] DWORD *pTargetLoad
);
```



## <a name="property-value"></a>Valor de propiedad

Número que representa la carga relativa de un destino.

## <a name="remarks"></a>Observaciones

El peso de una sesión pendiente con respecto a una sesión activa se puede cambiar estableciendo el valor del parámetro *lb \_ ConnectionEstablishmentPenalty* para el agente de conexión. Este parámetro se encuentra en la clave del registro **HKLM \\ System \\ CurrentControlSet \\ Services \\ Tssdis \\ Parameters** . El valor predeterminado de 1 especifica que las sesiones pendientes tienen el mismo peso que las sesiones activas.

Esta propiedad está disponible en Windows Server 2012 R2 con [KB3091411](https://support.microsoft.com/kb/3091411) instalado en la interfaz [**ITsSbTargetEx**](itssbtargetex.md) .

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
<td>Windows Server 2016<br/></td>
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
</dt> </dl>

 

 





