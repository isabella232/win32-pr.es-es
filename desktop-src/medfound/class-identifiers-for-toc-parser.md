---
description: Las siguientes clases se declaran y asocian a los identificadores de clase (CLSID) en wmcodecdsp. h.
ms.assetid: f82d92dc-fbce-4274-a10f-72fa8dd776cc
title: Identificadores de clase para el analizador de tabla de contenido (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5108855c687085e77ce36aa14b3424732e25572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677253"
---
# <a name="class-identifiers-for-table-of-contents-parser"></a>Identificadores de clase para el analizador de tabla de contenido

Las siguientes clases se declaran y asocian a los identificadores de clase (CLSID) en wmcodecdsp. h.



| Nombre de la clase       | Nombre descriptivo del objeto |
|------------------|----------------------|
| CTocEntry        | Entrada de TDC            |
| CTocEntryList    | Lista de entradas de TDC       |
| CToc             | TABLA DE CONTENIDO                  |
| CTocCollection   | Colección TOC       |
| CTocParser       | Analizador de TDC           |
| CTocGeneratorDmo | Generador de TDC        |



 

En la tabla anterior se proporciona un nombre de objeto descriptivo para cada clase. En esta documentación se usan esos nombres descriptivos para hacer referencia a las instancias de las clases. Por ejemplo, la documentación hace referencia a una instancia de la clase CTocEntry como un objeto de entrada de TDC.

En el código, puede usar **\_ \_ uuidof** para hacer referencia a los CLSID. Por ejemplo, puede usar el código siguiente para hacer referencia al CLSID de CTocGeneratorDmo.


```C++
__uuidof(CTocGeneratorDmo)
```



### <a name="clsid-constants-defined-in-wmcodecdsph"></a>Constantes CLSID definidas en Wmcodecdsp. h

Como alternativa al uso de **\_ \_ uuidof**, puede usar constantes para hacer referencia a los CLSID. Las siguientes constantes se definen en wmcodecdsp. h.



| Nombre de la clase     | Constante CLSID        |
|----------------|-----------------------|
| CTocEntry      | CLSID \_ CTocEntry      |
| CTocEntryList  | CLSID \_ CTocEntryList  |
| CToc           | CLSID \_ CToc           |
| CTocCollection | CLSID \_ CTocCollection |
| CTocParser     | CLSID \_ CTocParser     |



 

### <a name="clsid-constants-defined-in-wmcodecdspuuidlib"></a>Constantes CLSID definidas en Wmcodecdspuuid. lib

La siguiente constante CLSID se declara, pero no se define, en wmcodecdsp. h. Para usarlo en el código, debe vincular a wmcodecdspuuid. lib.



| Nombre de la clase       | Constante CLSID          |
|------------------|-------------------------|
| CTocGeneratorDmo | CLSID \_ CTocGeneratorDmo |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wmvdspa.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos de analizador de tabla de contenido](toc-parser-objects.md)
</dt> </dl>

 

 




