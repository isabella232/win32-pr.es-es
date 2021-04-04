---
title: Clave FileType
description: Usado por GetClassFile para comparar patrones con distintos bytes de archivo en un archivo no compuesto.
ms.assetid: ced23cdb-c184-43fe-ba37-fe1af8664b66
keywords:
- Clave del registro FileType COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a2e331588b627ee5ce9a9c1b69631f1e8a1dbe4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076288"
---
# <a name="filetype-key"></a>Clave FileType

Usado por [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) para comparar patrones con distintos bytes de archivo en un archivo no compuesto.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\FileType
   {CLSID}
      n = offset, cb, mask, value
```

<dl> <dt>

<span id="offset"></span><span id="OFFSET"></span>*posición*
</dt> <dd>

Determina la distancia desde el principio o el final del archivo hasta que comienza la comparación. Si el desplazamiento es un valor negativo, la comparación comienza desde el final del archivo menos el valor de desplazamiento. El valor de desplazamiento es un tipo decimal a menos que vaya precedido de "0x".

</dd> <dt>

<span id="cb"></span><span id="CB"></span>*CB*
</dt> <dd>

Representa la longitud en bytes desde el principio hasta el final del archivo. Representa el intervalo de bytes del archivo. El valor *CB* es un decimal a menos que esté precedido de "0x".

</dd> <dt>

<span id="mask"></span><span id="MASK"></span>*máscara*
</dt> <dd>

Valor binario utilizado para enmascaramiento, que se realiza mediante una operación AND lógica y el intervalo de bytes especificado por *offset* y *CB*. Si se omite este valor, los bytes se establecen en todos. Este valor siempre es hexadecimal.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*valor*
</dt> <dd>

Representa el patrón que debe coincidir para que un archivo sea de este tipo de archivo. El patrón se usa para identificar correctamente un formato de archivo conocido de su contenido, no de su extensión.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La función [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) usa las entradas para buscar coincidencias de patrones con distintos bytes de archivo en un archivo no compuesto. **Filetype** tiene subclaves CLSID, cada una de las cuales tiene una serie de subclaves **0**, **1**, **2**, **3**. Estos valores contienen patrones que, si coinciden, producen el CLSID indicado. Por ejemplo, un valor de "0, 4, FFFFFFFF, ABCD1234" indica que los cuatro primeros bytes deben ser ABCD1234, en ese orden. Un valor de "-4, 4, FEFEFEFE" indica que los últimos cuatro bytes del archivo deben ser FEFEFEFE. Si cualquiera de los patrones coincide, se devuelve el CLSID.

La clave **HKEY \_ local \_ Machine \\ software \\ classes** corresponde a la clave **\_ \_ raíz de las clases HKEY** , que se conserva por compatibilidad con versiones anteriores de com.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**<extensión de archivo \_>**](-file-extension--key.md)
</dt> <dt>

[**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile)
</dt> </dl>

 

 




