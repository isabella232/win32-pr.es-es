---
description: La interfaz IAMTimeline proporciona métodos para manipular la escala de tiempo, el objeto central de Microsoft DirectShow Editing Services (DES).
ms.assetid: 6750efa0-946c-4ad3-b0df-de55872b94c3
title: Interfaz IAMTimeline (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fc4374a198232625b87448004b667ccd8ce0183b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126892188"
---
# <a name="iamtimeline-interface"></a>IamTimeline (interfaz)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

La `IAMTimeline` interfaz proporciona métodos para manipular la escala de tiempo, el objeto central de Microsoft [DirectShow Editing Services](directshow-editing-services.md) (DES). Una escala de tiempo es una colección de elementos ordenados por el tiempo, como clips de vídeo, clips de audio, efectos y transiciones entre clips. El motor de representación usa la escala de tiempo para crear un gráfico de filtro, a partir del cual la aplicación puede generar la salida representada.

`IAMTimeline` realiza tres servicios básicos. It

-   Crea los objetos en la escala de tiempo.
-   Actúa como contenedor para esos objetos.
-   Establece y recupera los parámetros generales de la escala de tiempo.

Para crear el objeto de escala de tiempo, **llame a CoCreateInstance** con el identificador de clase CLSID \_ AMTimeline.

## <a name="members"></a>Members

La **interfaz IAMTimeline** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMTimeline** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IAMTimeline** tiene estos métodos.



| Método                                                             | Descripción                                                                                                                       |
|:-------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**AddGroup**](iamtimeline-addgroup.md)                           | Agrega un grupo a la escala de tiempo.<br/>                                                                                          |
| [**ClearAllGroups**](iamtimeline-clearallgroups.md)               | Quita todos los grupos de la escala de tiempo, junto con todos los objetos contenidos en esos grupos.<br/>                                |
| [**CreateEmptyNode**](iamtimeline-createemptynode.md)             | Crea un nuevo objeto de escala de tiempo.<br/>                                                                                         |
| [**EffectsEnabled**](iamtimeline-effectsenabled.md)               | Determina si los efectos están habilitados.<br/>                                                                                |
| [**EnableEffects**](iamtimeline-enableeffects.md)                 | Habilita o deshabilita todos los efectos de la escala de tiempo.<br/>                                                                       |
| [**EnableTransitions**](iamtimeline-enabletransitions.md)         | Habilita o deshabilita todas las transiciones de la escala de tiempo.<br/>                                                                   |
| [**GetCountOfType**](iamtimeline-getcountoftype.md)               | Recupera el número de objetos del tipo especificado contenidos en un grupo especificado y todos sus elementos secundarios.<br/> |
| [**GetDefaultEffect**](iamtimeline-getdefaulteffect.md)           | Recupera el efecto predeterminado.<br/>                                                                                          |
| [**GetDefaultEffectB**](iamtimeline-getdefaulteffectb.md)         | Recupera el efecto predeterminado como un **valor BSTR.**<br/>                                                                      |
| [**GetDefaultFPS**](iamtimeline-getdefaultfps.md)                 | Recupera la velocidad de fotogramas de salida predeterminada, en fotogramas por segundo.<br/>                                                         |
| [**GetDefaultTransition**](iamtimeline-getdefaulttransition.md)   | Recupera la transición predeterminada.<br/>                                                                                      |
| [**GetDefaultTransitionB**](iamtimeline-getdefaulttransitionb.md) | Recupera la transición predeterminada como un **valor BSTR.**<br/>                                                                  |
| [**GetDirtyRange**](iamtimeline-getdirtyrange.md)                 | No compatible.<br/>                                                                                                         |
| [**GetDuration**](iamtimeline-getduration.md)                     | Recupera la duración de la escala de tiempo.<br/>                                                                                       |
| [**GetDuration2**](iamtimeline-getduration2.md)                   | Recupera la duración de la escala de tiempo como **un valor double.**<br/>                                                                       |
| [**GetGroup**](iamtimeline-getgroup.md)                           | Recupera un grupo especificado.<br/>                                                                                           |
| [**GetGroupCount**](iamtimeline-getgroupcount.md)                 | Recupera el número de grupos contenidos en la escala de tiempo.<br/>                                                     |
| [**GetInsertMode**](iamtimeline-getinsertmode.md)                 | No compatible.<br/>                                                                                                         |
| [**IsDirty**](iamtimeline-isdirty.md)                             | No compatible.<br/>                                                                                                         |
| [**RemGroupFromList**](iamtimeline-remgroupfromlist.md)           | No compatible.<br/>                                                                                                         |
| [**SetDefaultEffect**](iamtimeline-setdefaulteffect.md)           | Establece el efecto predeterminado.<br/>                                                                                               |
| [**SetDefaultEffectB**](iamtimeline-setdefaulteffectb.md)         | Establece el efecto predeterminado como un **valor BSTR.**<br/>                                                                           |
| [**SetDefaultFPS**](iamtimeline-setdefaultfps.md)                 | Establece la velocidad de fotogramas de salida predeterminada, en fotogramas por segundo.<br/>                                                              |
| [**SetDefaultTransition**](iamtimeline-setdefaulttransition.md)   | Establece la transición predeterminada.<br/>                                                                                           |
| [**SetDefaultTransitionB**](iamtimeline-setdefaulttransitionb.md) | Establece la transición predeterminada como un valor BSTR.<br/>                                                                           |
| [**SetInsertMode**](iamtimeline-setinsertmode.md)                 | Sin implementar.<br/>                                                                                                       |
| [**SetInterestRange**](iamtimeline-setinterestrange.md)           | Sin implementar.<br/>                                                                                                       |
| [**TransitionsEnabled**](iamtimeline-transitionsenabled.md)       | Determina si las transiciones están habilitadas.<br/>                                                                            |
| [**ValidateSourceNames**](iamtimeline-validatesourcenames.md)     | Valida los nombres de origen en la escala de tiempo.<br/>                                                                                |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de Microsoft Windows para [Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 
