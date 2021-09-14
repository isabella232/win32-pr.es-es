---
title: Propiedad pluginName de ItsPubPlugin
description: Recupera el nombre del complemento.
ms.assetid: c1ea46b6-fac6-4140-a278-cb04ee9af739
ms.tgt_platform: multiple
keywords:
- propiedad pluginName Servicios de Escritorio remoto
- Propiedad pluginName Servicios de Escritorio remoto , interfaz ItsPubPlugin
- Interfaz ItsPubPlugin Servicios de Escritorio remoto , propiedad pluginName
topic_type:
- apiref
api_name:
- ItsPubPlugin.pluginName
- ItsPubPlugin.get_pluginName
api_location:
- Cpubplugin.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f5aa6ff6659047e9be48fd7b7a41f652c5cfd9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968160"
---
# <a name="itspubpluginpluginname-property"></a>Propiedad ItsPubPlugin::p luginName

Recupera el nombre del complemento.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_pluginName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valor de propiedad

Puntero a una variable **BSTR** para recibir el nombre del complemento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                         |
| IDL<br/>                      | <dl> <dt>Cpubplugin.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ItsPubPlugin**](/windows/desktop/api/tspubplugincom/nn-tspubplugincom-itspubplugin)
</dt> </dl>

 

 





