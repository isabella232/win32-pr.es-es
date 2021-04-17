---
description: Establece o recupera la ubicación de búsqueda de Active Directory.
ms.assetid: 43320799-1c01-4e09-bed9-f3576baadcce
title: Propiedad settings. ActiveDirectorySearchLocation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings.ActiveDirectorySearchLocation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d218b3d589b76980d468395a39452613aa57ada5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671094"
---
# <a name="settingsactivedirectorysearchlocation-property"></a>Propiedad settings. ActiveDirectorySearchLocation

\[La propiedad **ActiveDirectorySearchLocation** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.\]

La propiedad **ActiveDirectorySearchLocation** establece o recupera la ubicación de búsqueda Active Directory.

## <a name="syntax"></a>Sintaxis


```VB
Settings.ActiveDirectorySearchLocation As CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION
```



## <a name="property-value"></a>Valor de propiedad

Un valor de la enumeración de la [**\_ Ubicación de búsqueda de Active \_ Directory \_ \_ de CAPICOM**](capicom-active-directory-search-location.md) que especifica la ubicación de búsqueda. El valor predeterminado es CAPICOM \_ Search \_ any. En la siguiente tabla se muestran los valores posibles.



| Valor                                                                                                                                                                                                           | Significado                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="CAPICOM_SEARCH_ANY"></span><span id="capicom_search_any"></span><dl> <dt>**CAPICOM \_ Search \_ any**</dt> </dl>                                   | Buscar en todas las ubicaciones disponibles.<br/> |
| <span id="CAPICOM_SEARCH_DEFAULT_DOMAIN"></span><span id="capicom_search_default_domain"></span><dl> <dt>**\_ \_ dominio predeterminado de búsqueda de CAPICOM \_**</dt> </dl> | Buscar solo en el dominio predeterminado.<br/> |
| <span id="CAPICOM_SEARCH_GLOBAL_CATALOG"></span><span id="capicom_search_global_catalog"></span><dl> <dt>**CAPICOM \_ Buscar en el \_ \_ catálogo global**</dt> </dl> | Buscar solo en el catálogo global.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Configuración**](settings.md)
</dt> </dl>

 

 




