---
description: La propiedad FeatureRequestState es una propiedad de lectura y escritura del objeto de sesión.
ms.assetid: ba19603b-ac81-4a8b-81ca-ad5f28974599
title: Propiedad Session. FeatureRequestState
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679522"
---
# <a name="sessionfeaturerequeststate-property"></a>Propiedad Session. FeatureRequestState

La propiedad **FeatureRequestState** es una propiedad de lectura y escritura del objeto de [**sesión**](session-object.md) . Se puede usar para obtener el estado de acción actual de una característica o para solicitar un cambio en la acción de una característica y sus subcaracterísticas. La característica debe denominarse en la tabla de [características](feature-table.md) . Si se solicita un cambio en el estado de acción de una característica, también se puede cambiar el estado de la acción de todos los componentes de la característica cambiada. El estado de la acción de los componentes compartidos por más de una característica cambiará según corresponda según el nuevo estado de acción de la característica (vea la sección comentarios). La propiedad **FeatureRequestState** también se puede usar para configurar todas las características a la vez mediante la especificación de la palabra clave All en lugar de un nombre de característica específico.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Session.FeatureRequestState
Session.FeatureRequestState = propVal 
```



## <a name="property-value"></a>Valor de propiedad

Cadena requerida que especifica el nombre de la característica que se va a configurar. Para establecer todas las características en un estado de solicitud deseado, use la palabra reservada sin distinción de mayúsculas y minúsculas: todos.

## <a name="remarks"></a>Observaciones

Se debe llamar al método [**SetInstallLevel**](session-setinstalllevel.md) antes de llamar a **FeatureRequestState**.

Si se solicita el estado actual de la característica, la propiedad **FeatureRequestState** devuelve uno de los valores siguientes.



| Nombre del estado de selección         | Significado                                                               |
|------------------------------|-----------------------------------------------------------------------|
| msiInstallStateUnknown =-1  | No se realiza ninguna acción para la característica. Es equivalente a NULL.       |
| msiInstallStateAdvertised = 1 | La característica se va a anunciar.                                          |
| msiInstallStateAbsent = 2    | La característica se va a quitar.                                             |
| msiInstallStateLocal = 3     | La característica se instalará como de ejecución local.                              |
| msiInstallStateSource = 4    | La característica se instalará como ejecutar desde el origen.                        |
| msiInstallStateDefault = 5   | La característica se debe volver a instalar con el estado de acción actual de la característica. |



 

Por ejemplo, lo siguiente obtiene el estado actual de "función" de una acción personalizada de VBScript.


```VB
Dim iRequestState
iRequestState = Session.FeatureRequestState("MyFeature")
```



Si se está configurando el estado de la característica, la propiedad **FeatureRequestState** debe establecerse en uno de los valores siguientes.



| Nombre del estado de selección          | Significado                                 |
|-------------------------------|-----------------------------------------|
| msiInstallStateAdvertised = 1 | Anuncie la característica.                  |
| msiInstallStateAbsent = 2     | Quite la característica.                     |
| msiInstallStateLocal = 3      | Instale la característica como Run-local.       |
| msiInstallStateSource = 4     | Instale la característica como ejecutar desde el origen. |



 

Por ejemplo, las siguientes solicitudes de una acción personalizada de VBScript que "mi característica" se instalarán para ejecutarse localmente en el equipo.


```VB
Session.FeatureRequestState("MyFeature")=3
```



Cuando se llama a **FeatureRequestState** , el instalador intenta establecer el estado de la acción de cada componente asociado a la característica especificada en el estado especificado, lo mejor posible. Sin embargo, hay situaciones comunes en las que la solicitud no se puede respetar por completo. Por ejemplo, si una característica está asociada a dos componentes, el componente A y el componente B, a través de la tabla [FeatureComponents](featurecomponents-table.md) y el componente a tiene el atributo **msidbComponentAttributesLocalOnly** y el componente b tiene el atributo **msidbComponentAttributesSourceOnly** . En este caso, si se llama a **FeatureRequestState** con un estado solicitado de MsiInstallStateLocal o msiInstallStateSource, no se puede respetar la solicitud para ambos componentes. En este caso, ambos componentes se pueden activar con el componente a establecido en msiInstallStateLocal y el componente B establecido en msiInstallStateSource.

Si hay más de una característica vinculada a un único componente, el estado de acción final de ese componente se determina de la siguiente manera: si al menos una de las características llama a para que el componente se instale localmente, se instala msiInstallStateLocal. Si al menos una de las características llama a para que el componente se ejecute desde el medio de origen, se instala msiInstallStateSource. Si al menos una de las características llama a para quitar el componente, el estado de la acción es msiInstallStateAbsent. Para obtener más información sobre cómo se seleccionan las características para la instalación, vea la tabla de [características](feature-table.md) .

Si se produce un error en la propiedad, puede obtener información de error extendida mediante el método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | El IID \_ ISession se define como 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**De sesión**](session-object.md)
</dt> <dt>

[Característica](feature-table.md)
</dt> </dl>

 

 




