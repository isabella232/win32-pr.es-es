---
description: Establece o recupera la Active Directory de búsqueda.
ms.assetid: 43320799-1c01-4e09-bed9-f3576baadcce
title: Configuración. Propiedad ActiveDirectorySearchLocation
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160731"
---
# <a name="settingsactivedirectorysearchlocation-property"></a>Configuración. Propiedad ActiveDirectorySearchLocation

\[La **propiedad ActiveDirectorySearchLocation** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos.\]

La **propiedad ActiveDirectorySearchLocation** establece o recupera la Active Directory de búsqueda.

## <a name="syntax"></a>Sintaxis


```VB
Settings.ActiveDirectorySearchLocation As CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION
```



## <a name="property-value"></a>Valor de propiedad

Valor de la [**enumeración CAPICOM \_ ACTIVE DIRECTORY SEARCH \_ \_ \_ LOCATION**](capicom-active-directory-search-location.md) que especifica la ubicación de búsqueda. El valor predeterminado es CAPICOM \_ SEARCH \_ ANY. En la siguiente tabla se muestran los valores posibles.



| Valor                                                                                                                                                                                                           | Significado                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="CAPICOM_SEARCH_ANY"></span><span id="capicom_search_any"></span><dl> <dt>**CAPICOM \_ SEARCH \_ ANY**</dt> </dl>                                   | Buscar en todas las ubicaciones disponibles.<br/> |
| <span id="CAPICOM_SEARCH_DEFAULT_DOMAIN"></span><span id="capicom_search_default_domain"></span><dl> <dt>**DOMINIO PREDETERMINADO DE \_ CAPICOM \_ \_ SEARCH**</dt> </dl> | Busque solo el dominio predeterminado.<br/> |
| <span id="CAPICOM_SEARCH_GLOBAL_CATALOG"></span><span id="capicom_search_global_catalog"></span><dl> <dt>**CATÁLOGO GLOBAL DE CAPICOM \_ SEARCH \_ \_**</dt> </dl> | Busque solo el catálogo global.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Configuración**](settings.md)
</dt> </dl>

 

 




