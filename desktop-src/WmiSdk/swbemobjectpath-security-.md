---
description: La propiedad Security del objeto SWbemObjectPath se usa para obtener o establecer los componentes de seguridad de una ruta de acceso de objeto.
ms.assetid: 26e5e990-3b78-41b6-83c4-ba0d8b0d2f00
ms.tgt_platform: multiple
title: SWbemObjectPath.Security_ propiedad (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Security_
- ISWbemObjectPath.Security_
- ISWbemObjectPath.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ed473049de6973da077b1ccfabdd3fe752ff4e5edd13f4a49a7c5589309ae81e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639975"
---
# <a name="swbemobjectpathsecurity_-property"></a>Propiedad SWbemObjectPath.Security \_

La **propiedad Security** del objeto [**SWbemObjectPath**](swbemobjectpath.md) se usa para obtener o establecer los componentes de seguridad de una ruta de acceso de objeto. Tenga en cuenta que no se usa para establecer atributos de seguridad del propio **objeto SWbemObjectPath.** Solo se usa para representar los componentes de seguridad de la ruta de acceso de [**un objeto SWbemLocator.**](swbemlocator.md) Esta propiedad es un [**objeto SWbemSecurity.**](swbemsecurity.md)

> [!Note]  
> Establecer la [**propiedad Security \_**](swbemobject-security-.md) de un objeto [**SWbemObjectPath**](swbemobjectset.md) en **NULL** concede acceso ilimitado a todos los usuarios en todo momento. Para obtener más información, [**vea SWbemSecurity**](swbemsecurity.md).

 

Para obtener más información, [vea Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemObjectPath.Security_ As Object
```



## <a name="property-value"></a>Valor de propiedad

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectPath<br/>                                                       |
| IID<br/>                      | IID \_ ISWbemObjectPath<br/>                                                        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemObjectPath**](swbemobjectpath.md)
</dt> <dt>

[Crear una aplicación WMI o un script](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Establecer la seguridad \_ del proceso de la aplicación \_ cliente](setting-client-application-process-security.md)
</dt> </dl>

 

 




