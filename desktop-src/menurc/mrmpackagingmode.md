---
title: Enumeración MrmPackagingMode (MrmResourceIndexer.h)
description: Define constantes que especifican qué tipo de archivos PRI deben crear MrmCreateResourceFile y MrmCreateResourceFileInMemory.
ms.assetid: 5695B67E-5446-4538-83D2-F8FF91A5080E
keywords:
- Menús de enumeración MrmPackagingMode y otros recursos
topic_type:
- apiref
api_name:
- MrmPackagingMode
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58b4e968a43ba08786cc433b199bef5c07431420ac5942646530960279ea853e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117870154"
---
# <a name="mrmpackagingmode-enumeration"></a>Enumeración MrmPackagingMode

\[Parte de la información está relacionada con el producto publicado previamente que puede modificarse considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Define constantes que especifican qué tipo de archivos PRI deben crear [**MrmCreateResourceFile**](mrmcreateresourcefile.md) y [**MrmCreateResourceFileInMemory.**](mrmcreateresourcefileinmemory.md) Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, consulte API de indexación de recursos de paquetes (PRI) y sistemas [de compilación personalizados.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

## <a name="syntax"></a>Syntax


```C++
typedef enum _MrmPackagingMode { 
  MrmPackagingModeStandaloneFile  = 0,
  MrmPackagingModeAutoSplit       = 1,
  MrmPackagingModeResourcePack    = 2
} MrmPackagingMode;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MrmPackagingModeStandaloneFile"></span><span id="mrmpackagingmodestandalonefile"></span><span id="MRMPACKAGINGMODESTANDALONEFILE"></span>**MrmPackagingModeStandaloneFile**
</dt> <dd>

Especifica que se debe crear un único archivo PRI.

</dd> <dt>

<span id="MrmPackagingModeAutoSplit"></span><span id="mrmpackagingmodeautosplit"></span><span id="MRMPACKAGINGMODEAUTOSPLIT"></span>**MrmPackagingModeAutoSplit**
</dt> <dd>

Especifica que se deben crear varios archivos PRI; dividir automáticamente por todos los calificadores admitidos (específicamente, idioma y escala).

</dd> <dt>

<span id="MrmPackagingModeResourcePack"></span><span id="mrmpackagingmoderesourcepack"></span><span id="MRMPACKAGINGMODERESOURCEPACK"></span>**MrmPackagingModeResourcePack**
</dt> <dd>

Especifica que se debe crear un archivo PRI satélite de complemento.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1803 \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de servidor\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>MrmResourceIndexer.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

