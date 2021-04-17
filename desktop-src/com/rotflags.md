---
title: ROTFlags
description: Controla el registro de un servidor COM en la tabla de objetos en ejecución (ROT).
ms.assetid: a27c04e5-b1d3-4cb5-9b2c-9ae45663cf56
keywords:
- Valor del registro ROTFlags COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d52bc0c07ee6c86015ad1b997f2f21e33dda9a1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704617"
---
# <a name="rotflags"></a>ROTFlags

Controla el registro de un servidor COM en la tabla de objetos en ejecución (ROT).

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ROTFlags = flags
```

## <a name="remarks"></a>Observaciones

Se trata de un valor de **Registro \_ DWORD** .



| Valor de marca | Constante                        |
|------------|---------------------------------|
| 0x1        | **ROTREGFLAGS \_ ALLOWANYCLIENT** |



 

### <a name="rotregflags_allowanyclient-description"></a>ROTREGFLAGS \_ ALLOWANYCLIENT Descripción

Si un servidor COM desea registrarse en la tabla ROT y permitir que cualquier cliente tenga acceso al registro, debe usar la marca **ROTFLAGS \_ ALLOWANYCLIENT** . Un servidor COM "activar como activador" no puede especificar **ROTFLAGS \_ ALLOWANYCLIENT** porque el administrador de control de servicios (DCOMSCM) de DCOM aplica una comprobación de suplantación de identidad en esta marca. Por lo tanto, en Windows Vista y versiones posteriores, COM agrega compatibilidad con la entrada del registro **ROTFlags** que permite al servidor estipular que los registros de la tabla Rot estén disponibles para cualquier cliente.

La entrada debe existir en el subárbol del **\_ \_ equipo local HKEY** . Esta entrada proporciona un servidor "activar como activador" con la misma funcionalidad que **ROTFLAGS \_ ALLOWANYCLIENT** proporciona para un servidor runas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Clave AppID](appid-key.md)
</dt> <dt>

[Registrar servidores COM](registering-com-servers.md)
</dt> <dt>

[Seguridad en COM](security-in-com.md)
</dt> </dl>

 

 




