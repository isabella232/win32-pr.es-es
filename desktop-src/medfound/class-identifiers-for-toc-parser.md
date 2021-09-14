---
description: Las clases siguientes se declaran y asocian con identificadores de clase (CLID) en wmcodecdsp.h.
ms.assetid: f82d92dc-fbce-4274-a10f-72fa8dd776cc
title: Identificadores de clase para el analizador de tabla de contenido (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5108855c687085e77ce36aa14b3424732e25572
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127269359"
---
# <a name="class-identifiers-for-table-of-contents-parser"></a>Identificadores de clase para el analizador de tabla de contenido

Las clases siguientes se declaran y asocian con identificadores de clase (CLID) en wmcodecdsp.h.



| Nombre de la clase       | Nombre de objeto descriptivo |
|------------------|----------------------|
| CTocEntry        | Entrada de TOC            |
| CTocEntryList    | Lista de entradas de TOC       |
| CToc             | TABLA DE CONTENIDO                  |
| CTocCollection   | Colección de TOC       |
| CTocParser       | Analizador de TOC           |
| CTocGeneratorDmo | Generador de TOC        |



 

En la tabla anterior se proporciona un nombre de objeto descriptivo para cada clase. En esta documentación se usan esos nombres descriptivos para hacer referencia a instancias de las clases. Por ejemplo, la documentación hace referencia a una instancia de la clase CTocEntry como un objeto TOC Entry.

En el código, puede usar **\_ \_ uuidof** para hacer referencia a los CLID. Por ejemplo, puede usar el código siguiente para hacer referencia al CLSID para CTocGeneratorDmo.


```C++
__uuidof(CTocGeneratorDmo)
```



### <a name="clsid-constants-defined-in-wmcodecdsph"></a>Constantes CLSID definidas en Wmcodecdsp.h

Como alternativa al uso **\_ \_ de uuidof,** puede usar constantes para hacer referencia a los CLID. Las siguientes constantes se definen en wmcodecdsp.h



| Nombre de la clase     | ClSID constante        |
|----------------|-----------------------|
| CTocEntry      | CLSID \_ CTocEntry      |
| CTocEntryList  | CLSID \_ CTocEntryList  |
| CToc           | CLSID \_ CToc           |
| CTocCollection | CLSID \_ CTocCollection |
| CTocParser     | CLSID \_ CTocParser     |



 

### <a name="clsid-constants-defined-in-wmcodecdspuuidlib"></a>Constantes CLSID definidas en Wmcodecdspuuid.lib

La siguiente constante CLSID se declara, pero no se define, en wmcodecdsp.h. Para usarlo en el código, debe vincularlo a wmcodecdspuuid.lib.



| Nombre de la clase       | ClSID constante          |
|------------------|-------------------------|
| CTocGeneratorDmo | CLSID \_ CTocGeneratorDmo |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wmvdspa.dll</dt> </dl>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Objetos de analizador de tabla de contenido](toc-parser-objects.md)
</dt> </dl>

 

 




