---
title: Clave FileType
description: GetClassFile lo usa para buscar coincidencias de patrones con varios bytes de archivo en un archivo no compuesto.
ms.assetid: ced23cdb-c184-43fe-ba37-fe1af8664b66
keywords:
- Com de clave del Registro FileType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a2e331588b627ee5ce9a9c1b69631f1e8a1dbe4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973676"
---
# <a name="filetype-key"></a>Clave FileType

[**GetClassFile lo usa para**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) buscar coincidencias de patrones con varios bytes de archivo en un archivo no compuesto.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\FileType
   {CLSID}
      n = offset, cb, mask, value
```

<dl> <dt>

<span id="offset"></span><span id="OFFSET"></span>*Compensar*
</dt> <dd>

Determina la distancia desde el principio o el final del archivo para comenzar la comparación. Si el desplazamiento es un valor negativo, la comparación comienza desde el final del archivo menos el valor de desplazamiento. El valor de desplazamiento es un tipo decimal a menos que esté precedido de "0x".

</dd> <dt>

<span id="cb"></span><span id="CB"></span>*Cb*
</dt> <dd>

Representa la longitud en bytes desde el principio hasta el final del archivo. Representa el intervalo de bytes del archivo. El *valor cb* es un decimal a menos que esté precedido de "0x".

</dd> <dt>

<span id="mask"></span><span id="MASK"></span>*Máscara*
</dt> <dd>

Valor binario usado para enmascaramiento, que se realiza mediante una operación AND lógica, y el intervalo de bytes especificado por *offset* y *cb*. Si se omite este valor, los bytes se establecen en todos. Este valor siempre es hexadecimal.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*Valor*
</dt> <dd>

Representa el patrón que debe coincidir para que un archivo sea de este tipo de archivo. El patrón se usa para identificar correctamente un formato de archivo conocido a partir de su contenido, no por su extensión.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La función [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) usa entradas para buscar coincidencias con patrones con varios bytes de archivo en un archivo no compuesto. **FileType** tiene subclaves CLSID, cada una de las cuales tiene una serie de subclaves **0,** **1,** **2,** **3**. Estos valores contienen patrones que, si uno coincide, producen el CLSID indicado. Por ejemplo, un valor de "0, 4, FFFFFFFF, ABCD1234" indica que los primeros 4 bytes deben ser ABCD1234, en ese orden. Un valor de "-4, 4, FEFEFEFE" indica que los últimos cuatro bytes del archivo deben ser FEFEFEFE. Si alguno de los patrones coincide, se devuelve el CLSID.

La **clave HKEY \_ LOCAL MACHINE \_ SOFTWARE \\ \\ Classes** corresponde a la clave RAÍZ **HKEY \_ CLASSES, \_** que se conservaba por compatibilidad con versiones anteriores de COM.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**<extensión \_ de archivo>**](-file-extension--key.md)
</dt> <dt>

[**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile)
</dt> </dl>

 

 




