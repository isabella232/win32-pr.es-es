---
description: NLS incluye varias funciones de API que las aplicaciones pueden usar para asignar datos de configuración regional entre identificadores de configuración regional y nombres de configuración regional, y enumerar configuraciones regionales neutras.
ms.assetid: 01bc261d-dfee-430e-86c9-cfafe82856c8
title: Asignación de datos de configuración regional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1576844f13dda80a6b9d754fc807ef8a35514dcfedd88dc04cf233cfb2a1bfb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147198"
---
# <a name="mapping-locale-data"></a>Asignación de datos de configuración regional

NLS incluye varias funciones de API que las aplicaciones [](locale-identifiers.md) pueden usar para asignar datos de configuración regional entre identificadores de configuración regional y nombres de configuración [regional,](locale-names.md)y enumerar configuraciones regionales neutras. En este tema se describe el uso de estas funciones en Windows Vista y versiones posteriores y en sistemas operativos de vista previos Windows (a veces denominados "sistemas de nivel inferior").

## <a name="map-locale-data-on-windows-vista-and-later"></a>Asignar datos de configuración regional en Windows Vista y versiones posteriores

NLS proporciona varias funciones de asignación de configuración regional para que las usen las aplicaciones que desarrolle para ejecutarse en Windows Vista y versiones posteriores. También incluye funciones que las aplicaciones pueden usar para enumerar configuraciones regionales neutras.

**Usar las funciones de conversión estándar para la asignación de datos**

Para asignar entre un nombre de configuración regional y un identificador de configuración regional, la aplicación puede llamar a la [**función LocaleNameToLCID.**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) La aplicación usa [**LCIDToLocaleName para**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) asignar entre un identificador de configuración regional y un nombre de configuración regional.

**Enumerar configuraciones regionales neutras**

Para enumerar las configuraciones regionales neutras Windows 7 y versiones posteriores, la aplicación puede llamar a [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) con *dwFlags* establecido en [**LOCALE \_ NEUTRALDATA**](locale-neutraldata.md). También puede usar [**GetLocaleInfoEx con**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) *LCType* establecido en [**LOCALE \_ INEUTRAL**](locale-ineutral.md).

## <a name="map-locale-data-on-pre-windows-vista-operating-systems"></a>Asignación de datos de configuración regional en sistemas operativos Windows Vista

NLS incluye una biblioteca de vínculos directos (DLL) que se usa para las aplicaciones que desarrolla para ejecutarse en sistemas operativos Windows Vista. El archivo DLL admite funciones de conversión y enumeración para la asignación de datos.

> [!Note]  
> Las aplicaciones que solo se ejecutan Windows Vista y versiones posteriores no deben usar las funciones de asignación de nivel inferior ni de lista.

 

**Usar las funciones de conversión de nivel inferior para la asignación de datos**

La aplicación destinada a un sistema de nivel inferior puede llamar a la función [**DownlevelLCIDToLocaleName**](downlevellcidtolocalename.md) para convertir un identificador de configuración regional en un nombre de configuración regional. Si necesita convertir un nombre de configuración regional en un identificador de configuración regional, debe llamar a [**DownlevelLocaleNameToLCID**](downlevellocalenametolcid.md).

**Usar las funciones de lista de nivel inferior para enumerar las configuraciones regionales neutras**

La aplicación debe llamar a [**DownlevelGetParentLocaleLCID para**](downlevelgetparentlocalelcid.md) recuperar el identificador de configuración regional del elemento primario de una configuración regional. Si la aplicación necesita obtener el nombre de configuración regional del elemento primario de la configuración regional, debe llamar a [**DownlevelGetParentLocaleName**](downlevelgetparentlocalename.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la compatibilidad con idiomas nacionales](using-national-language-support.md)
</dt> <dt>

[Identificadores de configuración regional](locale-identifiers.md)
</dt> <dt>

[Nombres de configuración regional](locale-names.md)
</dt> </dl>

 

 



