---
title: Prefijos de URI
description: El prefijo del URI del recurso es diferente en función del esquema XML que describe el recurso.
ms.assetid: 47c32da6-98c9-4f66-82ac-647976127cb7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e73de4d6d1762e87aa05e72b6cb6b3fbb228b80d
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "103904888"
---
# <a name="uri-prefixes"></a>Prefijos de URI

El prefijo del [*URI del recurso*](windows-remote-management-glossary.md) es diferente en función del esquema XML que describe el recurso.

## <a name="prefixes"></a>Prefijos

Si obtiene acceso a una clase [*cim*](windows-remote-management-glossary.md) 2,1, como [**el \_ archivo de archivos CIM**](/windows/desktop/CIMWin32Prov/cim-datafile), el prefijo del URI difiere del prefijo de una clase CIM 2,9, **como \_ AdminDomain de CIM**. Las clases CIM 2,1 se documentan en la sección [clases CIM](/windows/desktop/WmiSdk/cimclas) de instrumental de administración de Windows (WMI).

La mayoría de [las clases de WMI](/windows/desktop/WmiSdk/wmi-classes) se encuentran en el espacio de nombres WMI de **\\ cimv2 raíz** . Las clases del proveedor de la interfaz de administración de plataforma inteligente ([IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)) de Microsoft se encuentran en el **\\ hardware raíz**.

La lista siguiente contiene los prefijos de URI de recurso para estos esquemas:

-   Clases WMI o CIM 2,1 en el espacio de nombres **root \\ cimv2**

    "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/"

-   Clases CIM 2,9 o clases IPMI

    "https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2"

-   Manera alternativa de obtener acceso a las clases del proveedor de IPMI

    "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/hardware/"

Para obtener más información, vea [URI de recursos](resource-uris.md) y cadenas de [UrlPrefix](/windows/desktop/Http/urlprefix-strings). Para obtener más información sobre cómo generar un URI para un método o una clase WMI, vea [administración remota de Windows y WMI](windows-remote-management-and-wmi.md).

## <a name="prefix-aliases"></a>Alias de prefijo

Un alias de prefijo es un acceso directo que representa el prefijo de URI de recurso largo. También puede utilizar alias en la línea de comandos de **WinRM** . Para ver una lista de los alias disponibles, escriba **alias de ayuda de WinRM**.

Tenga en cuenta que no se puede usar un alias dentro de una referencia de punto de conexión (EPR) al especificar un URI de recurso. Administración remota de Windows no puede expandir el alias cuando está incrustado en XML.

En el ejemplo de código siguiente, el alias de WinRM se usa en un EPR en lugar de en el URI de recurso completo, que es `http://schemas.microsoft.com/wbem/wsman/1/config/Listener` . En este caso, WinRM devuelve un error que indica que el servicio no puede procesar la solicitud.


```XML
ResourceUri = "</wxf:ResourceCreated>.....
<w:ResourceURI>winrm/config/listener</w:ResourceURI>...
</w:SelectorSet></a:ReferenceParameters></wxf:ResourceCreated>"

Set ResourceLocator = WSManObj.CreateResourceLocator(resourceUri)
ResponseStr = Session.Get(ResourceLocator, 0)
```



A continuación se enumeran los alias definidos y los URI de recursos para los que se sustituyen.

<dl> <dt>

<span id="wmi"></span><span id="WMI"></span>WMI
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

<span id="winrm"></span><span id="WINRM"></span>WinRM
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1`

</dd> <dt>

<span id="wsman"></span><span id="WSMAN"></span>wsman
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1`

</dd> <dt>

<span id="shell"></span><span id="SHELL"></span>interfaz
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/windows/shell`

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Administración remota de Windows](about-windows-remote-management.md)
</dt> <dt>

[Administración remota de Windows y WMI](windows-remote-management-and-wmi.md)
</dt> <dt>

[URI de recursos](resource-uris.md)
</dt> </dl>
