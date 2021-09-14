---
description: Realiza un seguimiento de las solicitudes secundarias que se generan a partir de una solicitud primaria.
ms.assetid: e1d98eae-6fc1-489b-aa8b-2e86bac5c65a
ms.tgt_platform: multiple
title: Interfaz IWbemCausalityAccess (Wbemint.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: db4c7a76b04b659cd467f7a4a7a9a8c1ba42721f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889209"
---
# <a name="iwbemcausalityaccess-interface"></a>Interfaz IWbemCausalityAccess

La **interfaz IWbemCausalityAccess** realiza un seguimiento de las solicitudes secundarias que se generan a partir de una solicitud primaria. Puede obtener un **objeto IWbemCausalityAccess** mediante una interfaz de consulta (QI) para [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext). Cada solicitud se identifica mediante un identificador único global (GUID) y puede tener una solicitud primaria o puede ser una solicitud principal. Un GUID es un número único de 128 bits. Por ejemplo, 5b2fc63a-8af4-44cb-960c-aefdced908d6.

## <a name="members"></a>Members

La **interfaz IWbemCausalityAccess** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWbemCausalityAccess** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IWbemCausalityAccess** tiene estos métodos.



| Método                                                    | Descripción                                                                                                                                                             |
|:----------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetRequestId**](iwbemcausalityaccess-getrequestid.md) | Devuelve un identificador GUID único para una solicitud.<br/>                                                                                                              |
| [**IsChildOf**](iwbemcausalityaccess-ischildof.md)       | Determina si una solicitud es un elemento secundario de una solicitud primaria especificada. Una solicitud primaria puede tener varias solicitudes secundarias, cada una identificada por un valor GUID único.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemint.h</dt> </dl>    |
| Archivo DLL<br/>                      | <dl> <dt>Fastprox.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[API COM para WMI](com-api-for-wmi.md)
</dt> </dl>

 

