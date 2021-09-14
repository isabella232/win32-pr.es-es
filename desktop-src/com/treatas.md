---
title: TreatAs
description: Especifica el CLSID de una clase que puede emular la clase actual.
ms.assetid: 1d7a1677-738a-4258-9afc-e77bd0dcf40f
keywords:
- Com de la clave del Registro TreatAs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4340b398d6a98b0445cee932da120e23355b71
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160535"
---
# <a name="treatas"></a>TreatAs

Especifica el CLSID de una clase que puede emular la clase actual.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      TreatAs = {CLSID_TreatAs}
```

## <a name="remarks"></a>Observaciones

Se trata de **un valor \_ REG SZ.**

La emulación es la capacidad de una aplicación de abrir y editar un objeto de una clase diferente, conservando al mismo tiempo el formato original del objeto. La resolución se produce en el equipo local, por lo que, en caso de activación remota, la resolución se produce en el equipo cliente mediante el CLSID especificado por **TreatAs**.

DCOM busca **treatas** en el registro local, incluso si se llama a la [**función CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) y se especifica un servidor remoto. Esto significa que si tiene una entrada **TreatAs** para Class1 que se tratará como Class2 en el equipo local, pero llama a **CoCreateInstance** para crear una instancia de Class1 y especifica un servidor remoto, DCOM intentará crear una instancia de Class2 en el servidor remoto, incluso si Class2 no está registrado en el servidor remoto, lo que provocará un error en la llamada a **CoCreateInstance.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**AutoTreatAs**](autotreatas.md)
</dt> <dt>

[**CoGetTreatAsClass**](/windows/desktop/api/combaseapi/nf-combaseapi-cogettreatasclass)
</dt> <dt>

[**CoTreatAsClass**](/windows/desktop/api/Objbase/nf-objbase-cotreatasclass)
</dt> </dl>

 

 




