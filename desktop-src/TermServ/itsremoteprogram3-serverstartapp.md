---
title: ITSRemoteProgram3 ServerStartApp, método
description: Especifica que una aplicación se inicie en la sesión remota.
ms.assetid: 55a05d05-66d5-48a1-b3a6-f087aeb62925
ms.tgt_platform: multiple
keywords:
- Método ServerStartApp Servicios de Escritorio remoto
- Método ServerStartApp Servicios de Escritorio remoto, interfaz ITSRemoteProgram3
- Interfaz ITSRemoteProgram3 Servicios de Escritorio remoto, método ServerStartApp
topic_type:
- apiref
api_name:
- ITSRemoteProgram3.ServerStartApp
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef1822fa98094870ebebe607528cdc69a8a201f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686171"
---
# <a name="itsremoteprogram3serverstartapp-method"></a>ITSRemoteProgram3:: ServerStartApp (método)

Especifica que una aplicación se inicie en la sesión remota.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ServerStartApp(
  [in] BSTR         bstrAppUserModelId,
  [in] BSTR         bstrArguments,
  [in] VARIANT_BOOL vbExpandEnvVarInArgumentsOnServer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrAppUserModelId* \[ de\]
</dt> <dd></dd> <dt>

*bstrArguments* \[ de\]
</dt> <dd></dd> <dt>

*vbExpandEnvVarInArgumentsOnServer* \[ de\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITSRemoteProgram3**](itsremoteprogram3.md)
</dt> </dl>

 

 





