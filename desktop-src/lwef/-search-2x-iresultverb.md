---
title: Interfaz IResultVerb (WdsSharedIDL. h)
description: Expone propiedades de verbo.
ms.assetid: 8cc8408e-0117-4344-ad26-0c4a5d09a935
keywords:
- Interfaz IResultVerb características del entorno heredado de Windows
- Interfaz IResultVerb características del entorno heredado de Windows, descritas
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
ms.openlocfilehash: d922b9e9b3eb93697ed7daf2688001b031db0c92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695968"
---
# <a name="iresultverb-interface"></a>Interfaz IResultVerb

> [!NOTE]
> Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar. 

Expone propiedades de verbo.

## <a name="members"></a>Miembros

La interfaz **IResultVerb** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IResultVerb** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La interfaz **IResultVerb** tiene estas propiedades.



| Propiedad                                                             | Tipo de acceso           | Descripción                                                                                                       |
|:---------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------|
| [**DisplayName**](-search-2x-iresultverb-displayname.md)<br/> | Solo lectura<br/>  | Esta propiedad devuelve un puntero al nombre para mostrar localizado del verbo. <br/>                           |
| [**DoIt**](-search-2x-iresultverb-doit.md)<br/>               | Solo escritura<br/> | Ejecuta el verbo. <br/>                                                                                    |
| [**habilitado**](-search-2x-iresultverb-enabled.md)<br/>         | Solo lectura<br/>  | Esta propiedad devuelve TRUE si el verbo está habilitado. <br/>                                                    |
| [**HelpText**](-search-2x-iresultverb-helptext.md)<br/>       | Solo lectura<br/>  | Esta propiedad devuelve un puntero a la cadena de ayuda localizada para el verbo. <br/>                            |
| [**Icono**](-search-2x-iresultverb-icon.md)<br/>               | Solo lectura<br/>  | Esta propiedad devuelve un puntero al identificador del icono opcional asociado al verbo. <br/>              |
| [**Name**](-search-2x-iresultverb-name.md)<br/>               | Solo lectura<br/>  | Esta propiedad devuelve un puntero al nombre de cononical para el verbo, como imprimir, abrir, etc. <br/> |



 

## <a name="remarks"></a>Observaciones

Estos métodos exponen propiedades y acciones aplicables a los verbos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP2 \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]<br/>                             |
| Redistribuible<br/>          | Búsqueda en el escritorio de Windows (WDS) 3,0<br/>                                               |
| Encabezado<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

