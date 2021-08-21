---
title: Propiedad RdpFileContents de IMsRdpClientShell
description: Especifica o recupera el contenido de Protocolo de escritorio remoto (RDP) que se va a iniciar desde Escritorio remoto Web Access (Acceso web de Escritorio remoto) o desde algún otro portal web.
ms.assetid: fcf37221-0fd5-41fd-83da-7fafc1aff944
ms.tgt_platform: multiple
keywords:
- Propiedad RdpFileContents Servicios de Escritorio remoto
- Propiedad RdpFileContents Servicios de Escritorio remoto , interfaz IMsRdpClientShell
- Interfaz IMsRdpClientShell Servicios de Escritorio remoto , propiedad RdpFileContents
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
ms.openlocfilehash: 121a2015b90def02342aede3342cca3566a9ed8fc7693f89b57a112f16869511
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118854449"
---
# <a name="imsrdpclientshellrdpfilecontents-property"></a>Propiedad IMsRdpClientShell::RdpFileContents

Especifica o recupera el contenido de Protocolo de escritorio remoto (RDP) que se va a iniciar desde Escritorio remoto Web Access (Acceso web de Escritorio remoto) o desde algún otro portal web.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


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
| IID<br/>                      | IID IMsRdpClientShell se define como \_ d012ae6d-c19a-4bfe-b367-201f8911f134<br/>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientShell**](imsrdpclientshell.md)
</dt> </dl>

 

 





