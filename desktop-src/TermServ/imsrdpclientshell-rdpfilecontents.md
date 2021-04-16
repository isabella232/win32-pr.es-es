---
title: Propiedad RdpFileContents de IMsRdpClientShell
description: Especifica o recupera el contenido del archivo Protocolo de escritorio remoto (RDP) que se va a iniciar desde Escritorio remoto Web Access (acceso web de escritorio remoto) o desde otro portal web.
ms.assetid: fcf37221-0fd5-41fd-83da-7fafc1aff944
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad RdpFileContents
- Propiedad RdpFileContents Servicios de Escritorio remoto, interfaz IMsRdpClientShell
- Servicios de Escritorio remoto de la interfaz IMsRdpClientShell, propiedad RdpFileContents
topic_type:
- apiref
api_name:
- IMsRdpClientShell.RdpFileContents
- IMsRdpClientShell.get_RdpFileContents
- IMsRdpClientShell.put_RdpFileContents
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed2d1c682c06415757f29f2226f48970f4268800
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686068"
---
# <a name="imsrdpclientshellrdpfilecontents-property"></a>IMsRdpClientShell:: RdpFileContents (propiedad)

Especifica o recupera el contenido del archivo Protocolo de escritorio remoto (RDP) que se va a iniciar desde Escritorio remoto Web Access (acceso web de escritorio remoto) o desde otro portal web.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_RdpFileContents(
  [in]  BSTR newVal
);

HRESULT get_RdpFileContents(
  [out] BSTR *pszRdpFile
);
```



## <a name="property-value"></a>Valor de propiedad

Especifica el contenido del archivo RDP que se va a iniciar desde el portal web.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClientShell se define como d012ae6d-c19a-4bfe-B367-201f8911f134<br/>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientShell**](imsrdpclientshell.md)
</dt> </dl>

 

 





