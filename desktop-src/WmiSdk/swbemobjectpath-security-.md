---
description: La propiedad Security del objeto SWbemObjectPath se usa para obtener o establecer los componentes de seguridad de una ruta de acceso de objeto.
ms.assetid: 26e5e990-3b78-41b6-83c4-ba0d8b0d2f00
ms.tgt_platform: multiple
title: Propiedad SWbemObjectPath.Security_ (Wbemdisp. h)
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
ms.openlocfilehash: 000f3f5e334ef0eba3dbd687d7bdc4b594442305
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276123"
---
# <a name="swbemobjectpathsecurity_-property"></a>Propiedad SWbemObjectPath. Security \_

La propiedad **Security** del objeto [**SWbemObjectPath**](swbemobjectpath.md) se usa para obtener o establecer los componentes de seguridad de una ruta de acceso de objeto. Tenga en cuenta que no se utiliza para establecer los atributos de seguridad del propio objeto **SWbemObjectPath** . Solo se usa para representar los componentes de seguridad de la ruta de acceso de un objeto [**SWbemLocator**](swbemlocator.md) . Esta propiedad es un objeto [**SWbemSecurity**](swbemsecurity.md) .

> [!Note]  
> Al establecer la propiedad [**\_ Security**](swbemobject-security-.md) de un objeto [**SWbemObjectPath**](swbemobjectset.md) en **null** , se concede acceso ilimitado a todos los usuarios en todo momento. Para obtener más información, vea [**SWbemSecurity**](swbemsecurity.md).

 

Para obtener más información, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemObjectPath.Security_ As Object
```



## <a name="property-value"></a>Valor de propiedad

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectPath<br/>                                                       |
| IID<br/>                      | \_ISWBEMOBJECTPATH IID<br/>                                                        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemObjectPath**](swbemobjectpath.md)
</dt> <dt>

[Crear una aplicación o un script WMI](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Establecer la \_ seguridad del proceso de la aplicación cliente \_](setting-client-application-process-security.md)
</dt> </dl>

 

 




