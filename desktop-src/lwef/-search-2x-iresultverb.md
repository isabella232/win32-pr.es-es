---
title: Interfaz IResultVerb (WdsSharedIDL.h)
description: Expone las propiedades del verbo.
ms.assetid: 8cc8408e-0117-4344-ad26-0c4a5d09a935
keywords:
- Características heredadas del entorno de Windows IResultVerb
- IResultVerb interface Legacy Windows Environment Features ,described
topic_type:
- apiref
api_name:
- IResultVerb
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b923d8a48f2be093edac60e8cb1a6186fd6b17725de7d860647594443e6ad197
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963605"
---
# <a name="iresultverb-interface"></a>Interfaz IResultVerb

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [API Windows Search en](../search/-search-reference-entry-page.md) su lugar. 

Expone las propiedades del verbo.

## <a name="members"></a>Miembros

La **interfaz IResultVerb** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IResultVerb** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **interfaz IResultVerb** tiene estas propiedades.



| Propiedad                                                             | Tipo de acceso           | Descripción                                                                                                       |
|:---------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------|
| [**DisplayName**](-search-2x-iresultverb-displayname.md)<br/> | Solo lectura<br/>  | Esta propiedad devuelve un puntero al nombre para mostrar localizado del verbo. <br/>                           |
| [**Doit**](-search-2x-iresultverb-doit.md)<br/>               | Solo escritura<br/> | Ejecuta el verbo . <br/>                                                                                    |
| [**habilitado**](-search-2x-iresultverb-enabled.md)<br/>         | Solo lectura<br/>  | Esta propiedad devuelve TRUE si el verbo está habilitado. <br/>                                                    |
| [**HelpText**](-search-2x-iresultverb-helptext.md)<br/>       | Solo lectura<br/>  | Esta propiedad devuelve un puntero a la cadena de ayuda localizada para el verbo. <br/>                            |
| [**Icono**](-search-2x-iresultverb-icon.md)<br/>               | Solo lectura<br/>  | Esta propiedad devuelve un puntero para controlar el icono opcional asociado al verbo . <br/>              |
| [**Nombre**](-search-2x-iresultverb-name.md)<br/>               | Solo lectura<br/>  | Esta propiedad devuelve un puntero al nombre cononical del verbo, como print, open, etc. <br/> |



 

## <a name="remarks"></a>Comentarios

Estos métodos exponen propiedades y acciones aplicables a verbos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de escritorio de SP2 \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Server 2003 solo con aplicaciones de escritorio de SP1 \[\]<br/>                             |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 3.0<br/>                                               |
| Header<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

