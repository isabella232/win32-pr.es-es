---
title: modificador/OLDNAMES
description: El modificador/OLDNAMES indica al compilador de MIDL que genere nombres de interfaz que no incluyan el número de versión.
ms.assetid: 3a79c399-e115-46fd-9559-681b85cd872d
keywords:
- /OLDNAMES modificador MIDL
topic_type:
- apiref
api_name:
- /oldnames
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44cf861d2bf4f4123d7a1ee103e6966e5d404946
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790234"
---
# <a name="oldnames-switch"></a>modificador/OLDNAMES

El modificador **/OLDNAMES** indica al compilador de MIDL que genere nombres de interfaz que no incluyan el número de versión.

``` syntax
midl /oldnames
```

## <a name="switch-options"></a>Opciones de conmutador

Este modificador no tiene parámetros.

## <a name="remarks"></a>Observaciones

El compilador MIDL incorpora el número de versión de la interfaz en el nombre de la interfaz que se genera en el código auxiliar (por ejemplo, iFace \_ v1 \_ 0 \_ ServerIfHandle). Este formato de nomenclatura es coherente con el formato usado por el compilador de OSF DCE IDL. Sin embargo, difiere del formato de nombres utilizado por el compilador MIDL 1,0. El compilador de MIDL 1,0 no incluyó números de versión en los nombres de interfaz (por ejemplo, iFace \_ ServerIfHandle). El modificador **/OLDNAMES** permite indicar al compilador de MIDL que genere nombres de interfaz que no incluyan el número de versión. De esta manera, el formato es coherente con los nombres generados por el compilador MIDL 1,0.

Si tiene código de aplicación de servidor escrito para su uso con un código auxiliar generado por el compilador de MIDL 1,0 y hace referencia al nombre de la interfaz generada por MIDL (por ejemplo, en una llamada a [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)), debe cambiarla para que haga referencia al estilo de nombre de interfaz admitido por la versión 2,0 o posterior del compilador de MIDL. Como alternativa, puede usar el modificador **/OLDNAMES** al invocar el compilador de MIDL.

## <a name="examples"></a>Ejemplos

**MIDL/OLDNAMES nombrearchivo. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> </dl>

 

 