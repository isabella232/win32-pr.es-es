---
title: Prefijos URI
description: El prefijo uri de recurso es diferente en función del esquema XML que describa el recurso.
ms.assetid: 47c32da6-98c9-4f66-82ac-647976127cb7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b44744d7ac7d158bd7d00423396681fef1499c94d61b5cb74a1dee48dad5c784
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898675"
---
# <a name="uri-prefixes"></a>Prefijos URI

El [*prefijo uri de*](windows-remote-management-glossary.md) recurso es diferente en función del esquema XML que describa el recurso.

## <a name="prefixes"></a>Prefijos

Si tiene acceso a una clase [*CIM*](windows-remote-management-glossary.md) 2.1, como [**CIM \_ DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile), el prefijo del URI difiere del prefijo de una clase CIM 2.9, como **CIM \_ AdminDomain**. Las clases CIM 2.1 se documentan en la sección [Clases CIM](/windows/desktop/WmiSdk/cimclas) de Windows Management Instrumentation (WMI).

La [mayoría de las clases WMI](/windows/desktop/WmiSdk/wmi-classes) están en el espacio de nombres WMI **\\ cimv2** raíz. Las clases para el proveedor de la Interfaz de administración de plataforma inteligente de Microsoft [(IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)están en **el hardware \\ raíz**.

La lista siguiente contiene los prefijos uri de recurso para estos esquemas:

-   Clases WMI o CIM 2.1 en el **espacio de nombres raíz \\ cimv2**

    "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/"

-   Clases CIM 2.9 o clases IPMI

    "https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2"

-   Manera alternativa de acceder a las clases de proveedor IPMI

    "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/hardware/"

Para obtener más información, vea [Uri de recursos](resource-uris.md) y [Cadenas UrlPrefix](/windows/desktop/Http/urlprefix-strings). Para obtener más información sobre cómo generar un URI para una clase o método WMI, [vea Windows Administración remota y WMI.](windows-remote-management-and-wmi.md)

## <a name="prefix-aliases"></a>Alias de prefijo

Un alias de prefijo es un acceso directo que representa el prefijo uri de recurso largo. También puede usar alias en la línea de comandos de **Winrm.** Para ver una lista de alias disponibles, escriba alias **de ayuda de Winrm.**

Tenga en cuenta que no se puede usar un alias dentro de una referencia de punto de conexión (EPR) al especificar un URI de recurso. Windows La administración remota no puede expandir el alias cuando está incrustado en XML.

En el ejemplo de código siguiente, el alias winrm se usa en un EPR en lugar del URI de recurso completo, que es `http://schemas.microsoft.com/wbem/wsman/1/config/Listener` . En este caso, WinRM devuelve un error que indica que el servicio no puede procesar la solicitud.


```XML
ResourceUri = "</wxf:ResourceCreated>.....
<w:ResourceURI>winrm/config/listener</w:ResourceURI>...
</w:SelectorSet></a:ReferenceParameters></wxf:ResourceCreated>"

Set ResourceLocator = WSManObj.CreateResourceLocator(resourceUri)
ResponseStr = Session.Get(ResourceLocator, 0)
```



A continuación se enumeran los alias definidos y los URI de recursos por los que sustituyen.

<dl> <dt>

<span id="wmi"></span><span id="WMI"></span>Wmi
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/wmi`

</dd> <dt>

<span id="wmicimv2"></span><span id="WMICIMV2"></span>wmicimv2
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2`

</dd> <dt>

<span id="cimv2"></span><span id="CIMV2"></span>cimv2
</dt> <dd>

`https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2`

</dd> <dt>

<span id="winrm"></span><span id="WINRM"></span>Winrm
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1`

</dd> <dt>

<span id="wsman"></span><span id="WSMAN"></span>wsman
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1`

</dd> <dt>

<span id="shell"></span><span id="SHELL"></span>Cáscara
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/windows/shell`

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Windows administración remota](about-windows-remote-management.md)
</dt> <dt>

[Windows Administración remota y WMI](windows-remote-management-and-wmi.md)
</dt> <dt>

[URI de recursos](resource-uris.md)
</dt> </dl>
