---
description: Especifica una palabra clave para un proveedor MFTrace.
ms.assetid: 1ce4a5ee-c053-4d31-a984-dc11acebbf2a
title: elemento keyword
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9df1f7a648e7861dc8d248141f051e9911c9cb93257f47fee5f2b4d2fd9d5469
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827555"
---
# <a name="keyword-element"></a>elemento keyword

Especifica una palabra clave para un [proveedor MFTrace.](mftrace.md)

## <a name="usage"></a>Uso

``` syntax
<keyword
  ID = "CDATA"/>
```

## <a name="attributes"></a>Atributos



| Atributo         | Tipo             | Requerido       | Descripción                                             |
|-------------------|------------------|----------------|---------------------------------------------------------|
| **Id**<br/> | CDATA<br/> | Sí<br/> | Nombre o máscara de la palabra clave<br/> <br/> |



## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios

| Elemento                                   |
|-------------------------------------------|
| [**mfdetours**](mfdetours.md)<br/> |
| [**Proveedor**](provider.md)<br/>   |



## <a name="remarks"></a>Comentarios

Para el [**elemento mfdetours,**](mfdetours.md) las palabras clave válidas se enumeran en el tema [Palabras clave de MFTrace](mftrace-keywords.md).

Para el [**elemento provider,**](provider.md) las palabras clave dependen del proveedor de eventos. Puede usar la utilidad Wevtutil.exe para enumerar las palabras clave de un proveedor determinado.

## <a name="element-information"></a>Información de elemento

:::row:::
    :::column:::
        Puede estar vacío
    :::column-end:::
    :::column span="2":::
        Sí
    :::column-end:::
:::row-end:::

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de configuración de MFTrace](mftrace-configuration-file.md)
</dt> <dt>

[Palabras clave de MFTrace](mftrace-keywords.md)
</dt> </dl>

 

 




