---
title: Tratar
description: Especifica el CLSID de una clase que puede emular la clase actual.
ms.assetid: 1d7a1677-738a-4258-9afc-e77bd0dcf40f
keywords:
- Clave del registro treatAs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4340b398d6a98b0445cee932da120e23355b71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903601"
---
# <a name="treatas"></a>Tratar

Especifica el CLSID de una clase que puede emular la clase actual.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      TreatAs = {CLSID_TreatAs}
```

## <a name="remarks"></a>Observaciones

Este es un valor de **reg \_ SZ** .

La emulación es la capacidad de una aplicación para abrir y editar un objeto de una clase diferente, a la vez que conserva el formato original del objeto. La resolución se produce en el equipo local, por lo que en el caso de la activación remota, la resolución se produce en el equipo cliente mediante el CLSID especificado por **treatAs**.

DCOM busca en el registro local los **tratados**, aunque llame a la función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) y especifique un servidor remoto. Esto significa que si tiene una entrada **treatAs** para que Class1 se trate como clase2 en el equipo local, pero llama a **CoCreateInstance** para crear una instancia de Class1 y especifica un servidor remoto, DCOM intentará crear una instancia de clase2 en el servidor remoto, incluso si clase2 no está registrado en el servidor remoto, lo que hará que se produzca un error en la llamada a **CoCreateInstance** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Autotreatas**](autotreatas.md)
</dt> <dt>

[**CoGetTreatAsClass**](/windows/desktop/api/combaseapi/nf-combaseapi-cogettreatasclass)
</dt> <dt>

[**CoTreatAsClass**](/windows/desktop/api/Objbase/nf-objbase-cotreatasclass)
</dt> </dl>

 

 




