---
description: La propiedad FeatureRequestState es una propiedad de lectura y escritura del objeto Session.
ms.assetid: ba19603b-ac81-4a8b-81ca-ad5f28974599
title: Propiedad Session.FeatureRequestState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureRequestState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1531157ab094d817d34650f8eae2ac6dc23c681c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063030"
---
# <a name="sessionfeaturerequeststate-property"></a>Propiedad Session.FeatureRequestState

La **propiedad FeatureRequestState** es una propiedad de lectura y escritura del [**objeto Session.**](session-object.md) Se puede usar para obtener el estado de acción actual de una característica o para solicitar un cambio en la acción de una característica y sus subatures. La característica debe tener un nombre en la [tabla](feature-table.md) Característica. Si se solicita un cambio en el estado de acción de una característica, también se puede cambiar el estado de acción de todos los componentes de la característica modificada. El estado de acción de los componentes compartidos por más de una característica se cambiará según corresponda en función del nuevo estado de acción de la característica (vea Comentarios). La **propiedad FeatureRequestState** también se puede usar para configurar todas las características a la vez especificando la palabra clave ALL en lugar de un nombre de característica específico.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Session.FeatureRequestState
Session.FeatureRequestState = propVal 
```



## <a name="property-value"></a>Valor de propiedad

Cadena necesaria que especifica el nombre de la característica que se va a configurar. Para establecer todas las características en un estado de solicitud deseado, use la palabra reservada sin mayúsculas y minúsculas: ALL.

## <a name="remarks"></a>Observaciones

Se [**debe llamar al método SetInstallLevel**](session-setinstalllevel.md) antes de llamar a **FeatureRequestState.**

Si se solicita el estado actual de la característica, la **propiedad FeatureRequestState** devuelve uno de los valores siguientes.



| Nombre del estado de selección         | Significado                                                               |
|------------------------------|-----------------------------------------------------------------------|
| msiInstallStateUnknown = -1  | No se hace ninguna acción para la característica. Esto equivale a null.       |
| msiInstallStateAdvertised =1 | La característica se va a anunciar.                                          |
| msiInstallStateAbsent = 2    | La característica se va a quitar.                                             |
| msiInstallStateLocal = 3     | La característica se debe instalar como run-local.                              |
| msiInstallStateSource = 4    | La característica se debe instalar como run-from-source.                        |
| msiInstallStateDefault = 5   | La característica se va a volver a instalar con el estado de acción actual de la característica. |



 

Por ejemplo, a continuación se obtiene el estado actual de "MyFeature" a partir de una acción personalizada de VBScript.


```VB
Dim iRequestState
iRequestState = Session.FeatureRequestState("MyFeature")
```



Si se configura el estado de la característica, la **propiedad FeatureRequestState** debe establecerse en uno de los valores siguientes.



| Nombre del estado de selección          | Significado                                 |
|-------------------------------|-----------------------------------------|
| msiInstallStateAdvertised = 1 | Anuncie la característica.                  |
| msiInstallStateAbsent = 2     | Quite la característica.                     |
| msiInstallStateLocal = 3      | Instale la característica como run-local.       |
| msiInstallStateSource = 4     | Instale la característica como run-from-source. |



 

Por ejemplo, las siguientes solicitudes de una acción personalizada de VBScript que "MyFeature" se instalan para ejecutarse localmente en el equipo.


```VB
Session.FeatureRequestState("MyFeature")=3
```



Cuando **se llama a FeatureRequestState,** el instalador intenta establecer el estado de acción de cada componente vinculado a la característica especificada en el estado especificado, lo mejor posible. Sin embargo, hay situaciones comunes en las que la solicitud no se puede respetar por completo. Por ejemplo, si una característica está vinculada a dos componentes, Componente A y Componente B, a través de la tabla [FeatureComponents](featurecomponents-table.md) y Componente A tiene el atributo **msidbComponentAttributesLocalOnly** y el componente B tiene el atributo **msidbComponentAttributesSourceOnly.** En este caso, si se llama a **FeatureRequestState** con un estado solicitado de msiInstallStateLocal o msiInstallStateSource, la solicitud no se puede respetar para ambos componentes. En este caso, ambos componentes pueden estar activados con el componente A establecido en msiInstallStateLocal y el componente B establecido en msiInstallStateSource.

Si hay más de una característica vinculada a un único componente, el estado de acción final de ese componente se determina de la siguiente manera: si al menos una característica llama a para que el componente se instale localmente, se instala msiInstallStateLocal. Si al menos una característica llama a para que el componente se ejecute desde el medio de origen, se instala msiInstallStateSource. Si al menos una característica requiere la eliminación del componente, el estado de acción es msiInstallStateAbsent. Para obtener más información sobre cómo se seleccionan las características para la instalación, vea la [tabla](feature-table.md) Características.

Si se produce un error en la propiedad , puede obtener información de error extendida mediante el [**método LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession se define como \_ 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Sesión**](session-object.md)
</dt> <dt>

[Característica](feature-table.md)
</dt> </dl>

 

 




