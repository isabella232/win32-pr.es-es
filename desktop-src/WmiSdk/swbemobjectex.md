---
description: Proporciona funcionalidad extendida para SWbemObject. Al igual que SWbemObject, todos los objetos WMI pueden usar los métodos de este objeto extendido.
ms.assetid: 944d4cdc-ad35-4b53-b755-f10131a087fb
ms.tgt_platform: multiple
title: Objeto SWbemObjectEx (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx
- SetFromText_
- ISWbemObjectEx
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 642b76cde4f4e27979dae0e930ec987dc9a02d36aa8d17c7dcdd9b8785204ac9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860155"
---
# <a name="swbemobjectex-object"></a>Objeto SWbemObjectEx

El **objeto SWbemObjectEx** proporciona una funcionalidad ampliada para [**SWbemObject.**](swbemobject.md) Al **igual que SWbemObject**, todos los objetos WMI pueden usar los métodos de este objeto extendido. La llamada [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) de VBScript no puede crear este objeto.

## <a name="members"></a>Miembros

El **objeto SWbemObjectEx** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto SWbemObjectEx** tiene estos métodos.



| Método                                      | Descripción                                                              |
|:--------------------------------------------|:-------------------------------------------------------------------------|
| [**GetText\_**](swbemobjectex-gettext-.md) | Devuelve un archivo de texto que muestra el contenido de un objeto en XML.<br/> |
| [**Actualizar\_**](swbemobjectex-refresh-.md) | Actualiza los datos de un objeto .<br/>                                  |
| **SetFromText\_**                           | Reservado para uso futuro.<br/>                                      |



 

### <a name="properties"></a>Propiedades

El **objeto SWbemObjectEx** tiene estas propiedades.



| Propiedad                                                                 | Tipo de acceso           | Descripción                                                                                                                                              |
|:-------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SystemProperties\_**](swbemobjectex-systemproperties-.md)<br/> | Lectura/escritura<br/> | Objeto [**SWbemPropertySet**](swbempropertyset.md) que contiene la colección de propiedades del sistema que se aplican a **SWbemObjectEx.**<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectEx<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemObjectEx<br/>                                                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos de API de scripting](scripting-api-objects.md)
</dt> <dt>

[**SWbemObject**](swbemobject.md)
</dt> <dt>

[WbemObjectTextFormatEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)
</dt> </dl>

 

