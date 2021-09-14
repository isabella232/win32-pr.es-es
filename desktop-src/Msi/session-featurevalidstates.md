---
description: La propiedad FeatureValidStates del objeto Session devuelve un entero que representa marcas de bits con cada bit pertinente que representa un estado de instalación válido para la característica especificada.
ms.assetid: 8a1f6911-b0a6-4fac-ba77-df4f1b7d15e2
title: Propiedad Session.FeatureValidStates
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureValidStates
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b76080bb7854c75cbfbb06697de9fc7d7a1af0c2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069640"
---
# <a name="sessionfeaturevalidstates-property"></a>Propiedad Session.FeatureValidStates

La **propiedad FeatureValidStates** del objeto [**Session**](session-object.md) devuelve un entero que representa marcas de bits con cada bit pertinente que representa un estado de instalación válido para la característica especificada.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Session.FeatureValidStates
```



## <a name="property-value"></a>Valor de propiedad

Nombre de cadena requerido del elemento de característica cuyos estados de instalación válidos se van a recuperar.

## <a name="remarks"></a>Observaciones

El valor devuelto se compone de marcas de bits como se muestra a continuación. Bit 0: si se establece, Local es un estado válido. Bit 1: si se establece, source es un estado válido.

La **propiedad FeatureValidStates** solo se realiza correctamente después de que el instalador haya llamado a las acciones [CostInitialize](costinitialize-action.md) [y CostFinalize.](costfinalize-action.md)

**FeatureValidStates determina** la validez del estado consultando todos los componentes que están vinculados a la característica especificada sin tener en cuenta el estado instalado actual de ningún componente.

Los posibles estados válidos para una característica se determinan de la siguiente manera:

-   Si la característica no contiene componentes, INSTALLSTATE \_ LOCAL y INSTALLSTATE \_ SOURCE son estados válidos para la característica.
-   Si al menos un componente de la característica tiene un atributo msidbComponentAttributesLocalOnly o msidbComponentAttributesOptional, INSTALLSTATE LOCAL es un estado válido para \_ la característica.
-   Si al menos un componente de la característica tiene un atributo msidbComponentAttributesSourceOnly o msidbComponentAttributesOptional, INSTALLSTATE SOURCE es un estado válido para \_ la característica.
-   Si se ha parcheado un archivo de un componente que pertenece a la característica o desde un origen comprimido, INSTALLSTATE SOURCE no se incluye como un estado válido \_ para la característica.
-   INSTALLSTATE ADVERTISE no es un estado válido si la característica no permite anuncios (msidbFeatureAttributesDisallowAdvertise) o la característica requiere compatibilidad con la plataforma para \_ anuncios (msidbFeatureAttributesNoUnsupportedAdvertise) y la plataforma no la admite.
-   INSTALLSTATE ABSENT es un estado válido para la característica si sus atributos no incluyen \_ msidbFeatureAttributesUIDisallowAbsent.
-   Los estados válidos de las características secundarias marcadas para seguir la característica primaria (msidbFeatureAttributesFollowParent) se basan en la acción o el estado instalado de la característica primaria.

Si se produce un error en la propiedad , puede obtener información de error extendida mediante el [**método LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession se define como \_ 000C109E-0000-0000-C000-00000000046<br/>                                                                                                                                                                             |



 

 




