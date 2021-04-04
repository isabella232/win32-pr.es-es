---
title: Tipos de exclusión mutua
description: Tipos de exclusión mutua
ms.assetid: bfe6cfe6-3df4-49c4-8015-fe4479b693c1
keywords:
- SDK de Windows Media Format, exclusión mutua
- Advanced Systems Format (ASF), exclusión mutua
- ASF (formato de sistemas avanzados), exclusión mutua
- exclusión mutua, tipos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c425e69c2aa3eac012874837a6970dbc26d1a51
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077276"
---
# <a name="mutual-exclusion-types"></a>Tipos de exclusión mutua

Puede usar tipos de exclusión mutua para identificar la naturaleza de un objeto de exclusión mutua en un perfil. Los tipos de exclusión mutua se usan como parámetros para [**IWMMutualExclusion:: GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-gettype) y [**IWMMutualExclusion:: SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype).

En la tabla siguiente se enumeran los identificadores de los tipos de exclusión mutua.



| Constante de tipo de exclusión mutua | GUID                                 |
|--------------------------------|--------------------------------------|
| \_Lenguaje WMMUTEX \_ CLSID       | D6E22A00-35DA-11D1-9034-00A0C90349BE |
| \_Velocidad de \_ bits WMMUTEX CLSID        | D6E22A01-35DA-11D1-9034-00A0C90349BE |
| \_Presentación de WMMUTEX CLSID \_   | D6E22A02-35DA-11D1-9034-00A0C90349BE |
| CLSID \_ WMMUTEX \_ desconocido        | D6E22A03-35DA-11D1-9034-00A0C90349BE |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Valores GUID**](guid-values.md)
</dt> </dl>

 

 




