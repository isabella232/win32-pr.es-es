---
description: NLS incluye una serie de funciones de API que las aplicaciones pueden usar para asignar datos de configuración regional entre los identificadores de configuración regional y los nombres de configuración regional, y para enumerar las configuraciones regionales neutras.
ms.assetid: 01bc261d-dfee-430e-86c9-cfafe82856c8
title: Asignar datos de configuración regional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec2b4ec93efab1cc9023bedfa5479c3a1fc81987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275764"
---
# <a name="mapping-locale-data"></a>Asignar datos de configuración regional

NLS incluye una serie de funciones de API que las aplicaciones pueden usar para asignar datos de configuración regional entre los [identificadores de configuración](locale-identifiers.md) regional y [los nombres de configuración regional](locale-names.md), y para enumerar las configuraciones regionales neutras. En este tema se describe el uso de estas funciones en Windows Vista y versiones posteriores y en los sistemas operativos anteriores a Windows Vista (a veces denominados "sistemas de nivel inferior").

## <a name="map-locale-data-on-windows-vista-and-later"></a>Asignar datos de configuración regional en Windows Vista y versiones posteriores

NLS proporciona varias funciones de asignación de configuración regional para que las usen las aplicaciones que desarrolle para ejecutarse en Windows Vista y versiones posteriores. También incluye funciones que las aplicaciones pueden usar para enumerar configuraciones regionales neutras.

**Usar las funciones de conversión estándar para la asignación de datos**

Para asignar entre un nombre de configuración regional y un identificador de configuración regional, la aplicación puede llamar a la función [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) . La aplicación usa [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) para asignar entre un identificador de configuración regional y un nombre de configuración regional.

**Enumerar configuraciones regionales neutras**

Para enumerar las configuraciones regionales neutras para Windows 7 y versiones posteriores, la aplicación puede llamar a [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) con *dwFlags* establecido en [**\_ NEUTRALDATA de configuración regional**](locale-neutraldata.md). También puede usar [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) con *LCType* establecido en [**configuración regional \_ INEUTRAL**](locale-ineutral.md).

## <a name="map-locale-data-on-pre-windows-vista-operating-systems"></a>Asignar datos de configuración regional en sistemas operativos anteriores a Windows Vista

NLS incluye una biblioteca de vínculos directos (DLL) que se utiliza para las aplicaciones que se desarrollan para ejecutarse en sistemas operativos anteriores a Windows Vista. El archivo DLL admite las funciones de conversión y enumeración para la asignación de datos.

> [!Note]  
> Las aplicaciones que solo se ejecutan en Windows Vista y versiones posteriores no deben usar las funciones de lista o asignación de nivel inferior.

 

**Usar las funciones de conversión de nivel inferior para la asignación de datos**

La aplicación destinada a un sistema de nivel inferior puede llamar a la función [**DownlevelLCIDToLocaleName**](downlevellcidtolocalename.md) para convertir un identificador de configuración regional en un nombre de configuración regional. Si necesita convertir un nombre de configuración regional en un identificador de configuración regional, debe llamar a [**DownlevelLocaleNameToLCID**](downlevellocalenametolcid.md).

**Usar las funciones de lista de bajo nivel para enumerar configuraciones regionales neutras**

La aplicación debe llamar a [**DownlevelGetParentLocaleLCID**](downlevelgetparentlocalelcid.md) para recuperar el identificador de configuración regional del elemento primario de una configuración regional. Si la aplicación necesita obtener el nombre de configuración regional del elemento primario para la configuración regional, debe llamar a [**DownlevelGetParentLocaleName**](downlevelgetparentlocalename.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la compatibilidad con National Language](using-national-language-support.md)
</dt> <dt>

[Identificadores de configuración regional](locale-identifiers.md)
</dt> <dt>

[Nombres de configuración regional](locale-names.md)
</dt> </dl>

 

 



