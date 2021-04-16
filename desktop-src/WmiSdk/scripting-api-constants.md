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
# <a name="scripting-api-constants"></a><span data-ttu-id="93f75-103">Scripting de constantes de API</span><span class="sxs-lookup"><span data-stu-id="93f75-103">Scripting API Constants</span></span>

<span data-ttu-id="93f75-104">WMI utiliza varios tipos de constantes en el parámetro *iflags* de llamadas de método en la [API de scripting para WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="93f75-104">WMI uses several types of constants in the *iflags* parameter of method calls in the [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

<span data-ttu-id="93f75-105">Visual Basic aplicaciones pueden incluir la biblioteca de tipos para la API de scripting, Wbemdisp. tlb.</span><span class="sxs-lookup"><span data-stu-id="93f75-105">Visual Basic applications can include the type library for the scripting API, Wbemdisp.tlb.</span></span> <span data-ttu-id="93f75-106">Los scripts no pueden tener acceso a las constantes de la biblioteca de tipos a menos que utilicen las <REFERENCE> <OBJECT> etiquetas o del formato de archivo XML de Windows Script Host (WSH), tal como se describe en [uso de la biblioteca de tipos de scripts de WMI](using-the-wmi-scripting-type-library.md).</span><span class="sxs-lookup"><span data-stu-id="93f75-106">Scripts are unable to access constants in the type library unless they use the <REFERENCE> or <OBJECT> tags from the Windows Script Host (WSH) XML file format as described in [Using the WMI Scripting Type Library](using-the-wmi-scripting-type-library.md).</span></span> <span data-ttu-id="93f75-107">De lo contrario, un script debe usar el valor de la constante.</span><span class="sxs-lookup"><span data-stu-id="93f75-107">Otherwise, a script must use the value of the constant.</span></span>

## <a name="constants"></a><span data-ttu-id="93f75-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="93f75-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="93f75-109"><span id="WbemAuthenticationLevelEnum"></span><span id="wbemauthenticationlevelenum"></span><span id="WBEMAUTHENTICATIONLEVELENUM"></span>[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)</span><span class="sxs-lookup"><span data-stu-id="93f75-109"><span id="WbemAuthenticationLevelEnum"></span><span id="wbemauthenticationlevelenum"></span><span id="WBEMAUTHENTICATIONLEVELENUM"></span>[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)</span></span>
</dt> <dd>

<span data-ttu-id="93f75-110">Defina los niveles de autenticación de seguridad.</span><span class="sxs-lookup"><span data-stu-id="93f75-110">Define the security authentication levels.</span></span>

</dd> <dt>

<span data-ttu-id="93f75-111"><span id="WbemChangeFlagEnum"></span><span id="wbemchangeflagenum"></span><span id="WBEMCHANGEFLAGENUM"></span>[**WbemChangeFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemchangeflagenum)</span><span class="sxs-lookup"><span data-stu-id="93f75-111"><span id="WbemChangeFlagEnum"></span><span id="wbemchangeflagenum"></span><span id="WBEMCHANGEFLAGENUM"></span>[**WbemChangeFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemchangeflagenum)</span></span>
</dt> <dd>

<span data-ttu-id="93f75-112">Defina cómo se lleva a cabo una operación de escritura en una clase o una instancia.</span><span class="sxs-lookup"><span data-stu-id="93f75-112">Define how a write operation to a class or an instance is carried out.</span></span>

</dd> <dt>

<span data-ttu-id="93f75-113"><span id="WbemCimTypeEnum"></span><span id="wbemcimtypeenum"></span><span id="WBEMCIMTYPEENUM"></span>[**WbemCimTypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)</span><span class="sxs-lookup"><span data-stu-id="93f75-113"><span id="WbemCimTypeEnum"></span><span id="wbemcimtypeenum"></span><span id="WBEMCIMTYPEENUM"></span>[**WbemCimTypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)</span></span>
</dt> <dd>

<span data-ttu-id="93f75-114">Defina los tipos de CIM válidos de un valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="93f75-114">Define the valid CIM types of a property value.</span></span>

</dd> <dt>

<span data-ttu-id="93f75-115"><span id="WbemComparisonFlagEnum"></span><span id="wbemcomparisonflagenum"></span><span id="WBEMCOMPARISONFLAGENUM"></span>[**WbemComparisonFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcomparisonflagenum)</span><span class="sxs-lookup"><span data-stu-id="93f75-115"><span id="WbemComparisonFlagEnum"></span><span id="wbemcomparisonflagenum"></span><span id="WBEMCOMPARISONFLAGENUM"></span>[**WbemComparisonFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcomparisonflagenum)</span></span>
</dt> <dd>

<span data-ttu-id="93f75-116">Defina la configuración para la comparación de objetos y se usa en [**SWbemObject. \_ CompareTo**](swbemobject-compareto-.md).</span><span class="sxs-lookup"><span data-stu-id="93f75-116">Define the settings for object comparison and are used by [**SWbemObject.CompareTo\_**](swbemobject-compareto-.md).</span></span>

</dd> <dt>

<span data-ttu-id="93f75-117"><span id="WbemConnectOptionsEnum"></span><span id="wbemconnectoptionsenum"></span><span id="WBEMCONNECTOPTIONSENUM"></span>[**WbemConnectOptionsEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemconnectoptionsenum)</span><span class="sxs-lookup"><span data-stu-id="93f75-117"><span id="WbemConnectOptionsEnum"></span><span id="wbemconnectoptionsenum"></span><span id="WBEMCONNECTOPTIONSENUM"></span>[**WbemConnectOptionsEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemconnectoptionsenum)</span></span>
</dt> <dd>

<span data-ttu-id="93f75-118">Define una marca de seguridad que se usa como parámetro en las llamadas al método [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) cuando se produce un error en una conexión a WMI en un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="93f75-118">Defines a security flag that is used as a parameter in calls to the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method when a connection to WMI on a remote machine is failing.</span></span>

</dd> <dt>

<span data-ttu-id="93f75-119"><span id="WbemErrorEnum"></span><span id="wbemerrorenum"></span><span id="WBEMERRORENUM"></span>[**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum)</span><span class="sxs-lookup"><span data-stu-id="93f75-119"><span id="WbemErrorEnum"></span><span id="wbemerrorenum"></span><span id="WBEMERRORENUM"></span>[**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum)</span></span>
</dt> <dd>

<span data-ttu-id="93f75-120">Defina los errores que pueden ser devueltos por las llamadas [API de scripting para WMI](scripting-api-for-wmi.md) .</span><span class="sxs-lookup"><span data-stu-id="93f75-120">Define the errors that may be returned by [Scripting API for WMI](scripting-api-for-wmi.md) calls.</span></span>

</dd> <dt>

<span data-ttu-id="93f75-121"><span id="WbemFlagEnum"></span><span id="wbemflagenum"></span><span id="WBEMFLAGENUM"></span>[**WbemFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)</span><span class="sxs-lookup"><span data-stu-id="93f75-121"><span id="WbemFlagEnum"></span><span id="wbemflagenum"></span><span id="WBEMFLAGENUM"></span>[**WbemFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)</span></span>
</dt> <dd>

<span data-ttu-id="93f75-122">Define las constantes que se usan en [**SWbemServices.ExecQuery**](swbemservices-execquery.md), [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md), [**SWbemServices. subclasses**](swbemservices-subclassesof.md)y [**SWbemServices. instances**](swbemservices-instancesof.md).</span><span class="sxs-lookup"><span data-stu-id="93f75-122">Defines constants that are used by [**SWbemServices.ExecQuery**](swbemservices-execquery.md), [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md), [**SWbemServices.SubclassesOf**](swbemservices-subclassesof.md), and [**SWbemServices.InstancesOf**](swbemservices-instancesof.md).</span></span>

</dd> <dt>

<span data-ttu-id="93f75-123"><span id="WbemImpersonationLevelEnum"></span><span id="wbemimpersonationlevelenum"></span><span id="WBEMIMPERSONATIONLEVELENUM"></span>[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)</span><span class="sxs-lookup"><span data-stu-id="93f75-123"><span id="WbemImpersonationLevelEnum"></span><span id="wbemimpersonationlevelenum"></span><span id="WBEMIMPERSONATIONLEVELENUM"></span>[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)</span></span>
</dt> <dd>

<span data-ttu-id="93f75-124">Defina los niveles de suplantación de seguridad.</span><span class="sxs-lookup"><span data-stu-id="93f75-124">Define the security impersonation levels.</span></span> <span data-ttu-id="93f75-125">Estas constantes se utilizan con [**SWbemSecurity**](swbemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="93f75-125">These constants are used with [**SWbemSecurity**](swbemsecurity.md).</span></span>

</dd> <dt>

<span data-ttu-id="93f75-126"><span id="WbemObjectTextFormatEnum"></span><span id="wbemobjecttextformatenum"></span><span id="WBEMOBJECTTEXTFORMATENUM"></span>[**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)</span><span class="sxs-lookup"><span data-stu-id="93f75-126"><span id="WbemObjectTextFormatEnum"></span><span id="wbemobjecttextformatenum"></span><span id="WBEMOBJECTTEXTFORMATENUM"></span>[**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)</span></span>
</dt> <dd>

<span data-ttu-id="93f75-127">Defina los formatos de texto de objeto válidos que va a usar [**SWbemObjectEx. gettext \_**](swbemobjectex-gettext-.md).</span><span class="sxs-lookup"><span data-stu-id="93f75-127">Define the valid object text formats to be used by [**SWbemObjectEx.GetText\_**](swbemobjectex-gettext-.md).</span></span>

</dd> <dt>

<span data-ttu-id="93f75-128"><span id="WbemPrivilegeEnum"></span><span id="wbemprivilegeenum"></span><span id="WBEMPRIVILEGEENUM"></span>[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)</span><span class="sxs-lookup"><span data-stu-id="93f75-128"><span id="WbemPrivilegeEnum"></span><span id="wbemprivilegeenum"></span><span id="WBEMPRIVILEGEENUM"></span>[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)</span></span>
</dt> <dd>

<span data-ttu-id="93f75-129">Defina los privilegios.</span><span class="sxs-lookup"><span data-stu-id="93f75-129">Define privileges.</span></span> <span data-ttu-id="93f75-130">Estas constantes se utilizan con [**SWbemSecurity**](swbemsecurity.md) para conceder los privilegios necesarios para algunas operaciones.</span><span class="sxs-lookup"><span data-stu-id="93f75-130">These constants are used with [**SWbemSecurity**](swbemsecurity.md) to grant the privileges required for some operations.</span></span>

</dd> <dt>

<span data-ttu-id="93f75-131"><span id="WbemQueryFlagEnum"></span><span id="wbemqueryflagenum"></span><span id="WBEMQUERYFLAGENUM"></span>[**WbemQueryFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemqueryflagenum)</span><span class="sxs-lookup"><span data-stu-id="93f75-131"><span id="WbemQueryFlagEnum"></span><span id="wbemqueryflagenum"></span><span id="WBEMQUERYFLAGENUM"></span>[**WbemQueryFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemqueryflagenum)</span></span>
</dt> <dd>

<span data-ttu-id="93f75-132">Defina la profundidad de enumeración o consulta, que determina el número de objetos que devuelve una llamada.</span><span class="sxs-lookup"><span data-stu-id="93f75-132">Define the depth of enumeration or query, which determines how many objects are returned by a call.</span></span>

</dd> <dt>

<span data-ttu-id="93f75-133"><span id="WbemTextFlagEnum"></span><span id="wbemtextflagenum"></span><span id="WBEMTEXTFLAGENUM"></span>[**WbemTextFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtextflagenum)</span><span class="sxs-lookup"><span data-stu-id="93f75-133"><span id="WbemTextFlagEnum"></span><span id="wbemtextflagenum"></span><span id="WBEMTEXTFLAGENUM"></span>[**WbemTextFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtextflagenum)</span></span>
</dt> <dd>

<span data-ttu-id="93f75-134">Define el contenido del texto del objeto generado y lo utiliza [**SWbemObject. GetObjectText \_**](swbemobject-getobjecttext-.md).</span><span class="sxs-lookup"><span data-stu-id="93f75-134">Defines the content of generated object text and is used by [**SWbemObject.GetObjectText\_**](swbemobject-getobjecttext-.md).</span></span>

</dd> <dt>

<span data-ttu-id="93f75-135"><span id="WbemTimeout"></span><span id="wbemtimeout"></span><span id="WBEMTIMEOUT"></span>[**WbemTimeout**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtimeout)</span><span class="sxs-lookup"><span data-stu-id="93f75-135"><span id="WbemTimeout"></span><span id="wbemtimeout"></span><span id="WBEMTIMEOUT"></span>[**WbemTimeout**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtimeout)</span></span>
</dt> <dd>

<span data-ttu-id="93f75-136">Define las constantes de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="93f75-136">Defines the time-out constants.</span></span> <span data-ttu-id="93f75-137">[**SWbemEventSource. NextEvent**](swbemeventsource-nextevent.md)usa esta constante.</span><span class="sxs-lookup"><span data-stu-id="93f75-137">This constant is used by [**SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md).</span></span>

</dd> </dl>

## <a name="combining-flags"></a><span data-ttu-id="93f75-138">Combinar marcas</span><span class="sxs-lookup"><span data-stu-id="93f75-138">Combining Flags</span></span>

<span data-ttu-id="93f75-139">Puede combinar marcas para afectar a más de un aspecto de la llamada API.</span><span class="sxs-lookup"><span data-stu-id="93f75-139">You can combine flags to affect more than one aspect of the API call.</span></span>

<span data-ttu-id="93f75-140">Por ejemplo, para crear una llamada [*semisincrónica*](gloss-s.md) , el parámetro *iFlags* de una llamada a [**SWbemServices.Exe\_ CQuery**](swbemservices-execquery.md) debe contener dos marcas: **WbemFlagReturnImmediately** y **WbemFlagForwardOnly**.</span><span class="sxs-lookup"><span data-stu-id="93f75-140">For example, to create a [*semisynchronous*](gloss-s.md) call, the *iFlags* parameter in an [**SWbemServices.ExecQuery\_**](swbemservices-execquery.md) call must contain two flags: **WbemFlagReturnImmediately** and **WbemFlagForwardOnly**.</span></span> <span data-ttu-id="93f75-141">El valor de **WbemFlagReturnImmediately** es 16 y el valor de **WbemFlagForwardOnly** es 32.</span><span class="sxs-lookup"><span data-stu-id="93f75-141">The value of **WbemFlagReturnImmediately** is 16 and the value of **WbemFlagForwardOnly** is 32.</span></span> <span data-ttu-id="93f75-142">Dado que no se puede tener acceso a las constantes por su nombre, se combinan los valores de estas marcas, lo que produce un valor de *iFlags* de 48.</span><span class="sxs-lookup"><span data-stu-id="93f75-142">Because the constants cannot be accessed by name, the values of these flags are combined, producing an *iFlags* value of 48.</span></span>

<span data-ttu-id="93f75-143">En el siguiente ejemplo de script se muestra la llamada a.</span><span class="sxs-lookup"><span data-stu-id="93f75-143">The following script example shows the call.</span></span>


```VB
On Error Resume Next
For Each obj in GetObject("WinMgmts:").ExecQuery _
("SELECT * FROM Win32_NTLogEvent WHERE _ LogFile='Application'",,48)
    count  = count + 1
Next
```



<span data-ttu-id="93f75-144">No todas las marcas se pueden combinar porque muchas se excluyen mutuamente y pueden producir resultados imprevisibles.</span><span class="sxs-lookup"><span data-stu-id="93f75-144">Not all flags can be combined since many are mutually exclusive and may produce unpredictable results.</span></span>

## <a name="related-topics"></a><span data-ttu-id="93f75-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="93f75-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93f75-146">API de scripting para WMI</span><span class="sxs-lookup"><span data-stu-id="93f75-146">Scripting API for WMI</span></span>](scripting-api-for-wmi.md)
</dt> </dl>

 

 



