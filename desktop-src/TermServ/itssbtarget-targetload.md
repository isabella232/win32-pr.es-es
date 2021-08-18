---
title: Propiedad TargetLoad de ITsSbTarget
description: Recupera la carga relativa en un destino.
ms.assetid: 56618dcf-1319-4310-80ba-7ed71b8b02e8
ms.tgt_platform: multiple
keywords:
- Propiedades TargetLoad Servicios de Escritorio remoto
- Propiedad TargetLoad Servicios de Escritorio remoto , interfaz ITsSbTarget
- Interfaz ITsSbTarget Servicios de Escritorio remoto , propiedad TargetLoad
- Propiedad TargetLoad Servicios de Escritorio remoto , interfaz ITsSbTargetEx
- Interfaz ITsSbTargetEx Servicios de Escritorio remoto , propiedad TargetLoad
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
ms.openlocfilehash: 3c367e9c00caff78bb3e64263c1622de45fa6e640e78d88239e1ed25a6f68558
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989865"
---
# <a name="itssbtargettargetload-property"></a>Propiedad ITsSbTarget::TargetLoad

Recupera la carga relativa en un destino. Este valor se basa en el número de sesiones existentes y pendientes. De forma predeterminada, una sesión pendiente tiene el mismo valor que una sesión existente.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_TargetLoad(
  [out, retval] DWORD *pTargetLoad
);
```



## <a name="property-value"></a>Valor de propiedad

Número que representa la carga relativa en un destino.

## <a name="remarks"></a>Comentarios

El peso de una sesión pendiente con respecto a una sesión activa se puede cambiar estableciendo el valor del parámetro *\_ LB ConnectionEstablishmentPenalty* para el Agente de conexión. Este parámetro se encuentra en la clave del Registro **HKLM \\ System \\ CurrentControlSet \\ Services \\ Tssdis \\ Parameters.** El valor predeterminado de 1 especifica que las sesiones pendientes tienen el mismo peso que las sesiones activas.

Esta propiedad está disponible en Windows Server 2012 R2 con [KB3091411](https://support.microsoft.com/kb/3091411) instalado en la [**interfaz ITsSbTargetEx.**](itssbtargetex.md)

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
<td>Idl<br/></td>
<td><dl> <dt>Sbtsv.idl</dt> </dl></td>
</tr>
<tr class="even">
<td>IID<br/></td>
<td>IID_ITsSbTarget se define como:
<ul>
<li>16616ECC-272D-411D-B324-126893033856</li>
<li>e85e10ea-db0b-4752-b456-5fd5840901c0 en Windows Server 2008 R2</li>
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

 

 





