---
description: La API de scripting para WMI contiene marcas, valores comunes y códigos de error.
ms.assetid: feaab757-3167-420b-8f42-edced4cd4c53
ms.tgt_platform: multiple
title: Scripting de constantes de API
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8576d4c7ab5b6103efca4491bc00b2fcf4649ef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706089"
---
# <a name="scripting-api-constants"></a>Scripting de constantes de API

WMI utiliza varios tipos de constantes en el parámetro *iflags* de llamadas de método en la [API de scripting para WMI](scripting-api-for-wmi.md).

Visual Basic aplicaciones pueden incluir la biblioteca de tipos para la API de scripting, Wbemdisp. tlb. Los scripts no pueden tener acceso a las constantes de la biblioteca de tipos a menos que utilicen las <REFERENCE> <OBJECT> etiquetas o del formato de archivo XML de Windows Script Host (WSH), tal como se describe en [uso de la biblioteca de tipos de scripts de WMI](using-the-wmi-scripting-type-library.md). De lo contrario, un script debe usar el valor de la constante.

## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WbemAuthenticationLevelEnum"></span><span id="wbemauthenticationlevelenum"></span><span id="WBEMAUTHENTICATIONLEVELENUM"></span>[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dd>

Defina los niveles de autenticación de seguridad.

</dd> <dt>

<span id="WbemChangeFlagEnum"></span><span id="wbemchangeflagenum"></span><span id="WBEMCHANGEFLAGENUM"></span>[**WbemChangeFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemchangeflagenum)
</dt> <dd>

Defina cómo se lleva a cabo una operación de escritura en una clase o una instancia.

</dd> <dt>

<span id="WbemCimTypeEnum"></span><span id="wbemcimtypeenum"></span><span id="WBEMCIMTYPEENUM"></span>[**WbemCimTypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)
</dt> <dd>

Defina los tipos de CIM válidos de un valor de propiedad.

</dd> <dt>

<span id="WbemComparisonFlagEnum"></span><span id="wbemcomparisonflagenum"></span><span id="WBEMCOMPARISONFLAGENUM"></span>[**WbemComparisonFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcomparisonflagenum)
</dt> <dd>

Defina la configuración para la comparación de objetos y se usa en [**SWbemObject. \_ CompareTo**](swbemobject-compareto-.md).

</dd> <dt>

<span id="WbemConnectOptionsEnum"></span><span id="wbemconnectoptionsenum"></span><span id="WBEMCONNECTOPTIONSENUM"></span>[**WbemConnectOptionsEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemconnectoptionsenum)
</dt> <dd>

Define una marca de seguridad que se usa como parámetro en las llamadas al método [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) cuando se produce un error en una conexión a WMI en un equipo remoto.

</dd> <dt>

<span id="WbemErrorEnum"></span><span id="wbemerrorenum"></span><span id="WBEMERRORENUM"></span>[**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum)
</dt> <dd>

Defina los errores que pueden ser devueltos por las llamadas [API de scripting para WMI](scripting-api-for-wmi.md) .

</dd> <dt>

<span id="WbemFlagEnum"></span><span id="wbemflagenum"></span><span id="WBEMFLAGENUM"></span>[**WbemFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)
</dt> <dd>

Define las constantes que se usan en [**SWbemServices.ExecQuery**](swbemservices-execquery.md), [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md), [**SWbemServices. subclasses**](swbemservices-subclassesof.md)y [**SWbemServices. instances**](swbemservices-instancesof.md).

</dd> <dt>

<span id="WbemImpersonationLevelEnum"></span><span id="wbemimpersonationlevelenum"></span><span id="WBEMIMPERSONATIONLEVELENUM"></span>[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dd>

Defina los niveles de suplantación de seguridad. Estas constantes se utilizan con [**SWbemSecurity**](swbemsecurity.md).

</dd> <dt>

<span id="WbemObjectTextFormatEnum"></span><span id="wbemobjecttextformatenum"></span><span id="WBEMOBJECTTEXTFORMATENUM"></span>[**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)
</dt> <dd>

Defina los formatos de texto de objeto válidos que va a usar [**SWbemObjectEx. gettext \_**](swbemobjectex-gettext-.md).

</dd> <dt>

<span id="WbemPrivilegeEnum"></span><span id="wbemprivilegeenum"></span><span id="WBEMPRIVILEGEENUM"></span>[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dd>

Defina los privilegios. Estas constantes se utilizan con [**SWbemSecurity**](swbemsecurity.md) para conceder los privilegios necesarios para algunas operaciones.

</dd> <dt>

<span id="WbemQueryFlagEnum"></span><span id="wbemqueryflagenum"></span><span id="WBEMQUERYFLAGENUM"></span>[**WbemQueryFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemqueryflagenum)
</dt> <dd>

Defina la profundidad de enumeración o consulta, que determina el número de objetos que devuelve una llamada.

</dd> <dt>

<span id="WbemTextFlagEnum"></span><span id="wbemtextflagenum"></span><span id="WBEMTEXTFLAGENUM"></span>[**WbemTextFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtextflagenum)
</dt> <dd>

Define el contenido del texto del objeto generado y lo utiliza [**SWbemObject. GetObjectText \_**](swbemobject-getobjecttext-.md).

</dd> <dt>

<span id="WbemTimeout"></span><span id="wbemtimeout"></span><span id="WBEMTIMEOUT"></span>[**WbemTimeout**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtimeout)
</dt> <dd>

Define las constantes de tiempo de espera. [**SWbemEventSource. NextEvent**](swbemeventsource-nextevent.md)usa esta constante.

</dd> </dl>

## <a name="combining-flags"></a>Combinar marcas

Puede combinar marcas para afectar a más de un aspecto de la llamada API.

Por ejemplo, para crear una llamada [*semisincrónica*](gloss-s.md) , el parámetro *iFlags* de una llamada a [**SWbemServices.Exe\_ CQuery**](swbemservices-execquery.md) debe contener dos marcas: **WbemFlagReturnImmediately** y **WbemFlagForwardOnly**. El valor de **WbemFlagReturnImmediately** es 16 y el valor de **WbemFlagForwardOnly** es 32. Dado que no se puede tener acceso a las constantes por su nombre, se combinan los valores de estas marcas, lo que produce un valor de *iFlags* de 48.

En el siguiente ejemplo de script se muestra la llamada a.


```VB
On Error Resume Next
For Each obj in GetObject("WinMgmts:").ExecQuery _
("SELECT * FROM Win32_NTLogEvent WHERE _ LogFile='Application'",,48)
    count  = count + 1
Next
```



No todas las marcas se pueden combinar porque muchas se excluyen mutuamente y pueden producir resultados imprevisibles.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[API de scripting para WMI](scripting-api-for-wmi.md)
</dt> </dl>

 

 



