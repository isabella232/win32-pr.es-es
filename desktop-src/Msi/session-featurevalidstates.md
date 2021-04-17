---
description: La propiedad FeatureValidStates del objeto de sesión devuelve un entero que representa las marcas de bits con cada bit pertinente que representa un estado de instalación válido de la característica especificada.
ms.assetid: 8a1f6911-b0a6-4fac-ba77-df4f1b7d15e2
title: Propiedad Session. FeatureValidStates
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653826"
---
# <a name="sessionfeaturevalidstates-property"></a>Propiedad Session. FeatureValidStates

La propiedad **FeatureValidStates** del objeto de [**sesión**](session-object.md) devuelve un entero que representa las marcas de bits con cada bit pertinente que representa un estado de instalación válido de la característica especificada.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Session.FeatureValidStates
```



## <a name="property-value"></a>Valor de propiedad

Nombre de cadena necesario del elemento de característica cuyos Estados de instalación válidos se van a recuperar.

## <a name="remarks"></a>Observaciones

El valor devuelto se compone de marcas de bits como se indica a continuación. Bit 0: si se establece, local es un estado válido. Bit 1: si se establece, el origen es un estado válido.

La propiedad **FeatureValidStates** solo se realiza correctamente después de que el instalador haya llamado a las acciones [CostInitialize](costinitialize-action.md) y [CostFinalize](costfinalize-action.md) .

**FeatureValidStates** determina la validez del estado mediante la consulta de todos los componentes que están vinculados a la característica especificada sin tener en cuenta el estado de instalación actual de ningún componente.

Los posibles estados válidos para una característica se determinan de la siguiente manera:

-   Si la característica no contiene componentes, tanto \_ \_ el origen de installstate local como el de installstate son Estados válidos para la característica.
-   Si al menos un componente de la característica tiene un atributo de msidbComponentAttributesLocalOnly o msidbComponentAttributesOptional, INSTALLSTATE \_ local es un estado válido para la característica.
-   Si al menos un componente de la característica tiene un atributo de msidbComponentAttributesSourceOnly o msidbComponentAttributesOptional, \_ el origen de INSTALLSTATE es un estado válido para la característica.
-   Si se aplica una revisión a un archivo de un componente que pertenece a la característica o desde un origen comprimido, \_ el origen de INSTALLSTATE no se incluye como un estado válido para la característica.
-   INSTALLSTATE \_ anunciar no es un estado válido si la característica no permite el anuncio (msidbFeatureAttributesDisallowAdvertise) o la característica requiere compatibilidad con la plataforma para el anuncio (msidbFeatureAttributesNoUnsupportedAdvertise) y la plataforma no lo admite.
-   INSTALLSTATE \_ ausente es un estado válido para la característica si sus atributos no incluyen msidbFeatureAttributesUIDisallowAbsent.
-   Los Estados válidos para las características secundarias marcadas para seguir la característica primaria (msidbFeatureAttributesFollowParent) se basan en la acción o el estado instalado de la característica primaria.

Si se produce un error en la propiedad, puede obtener información de error extendida mediante el método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | El IID \_ ISession se define como 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




