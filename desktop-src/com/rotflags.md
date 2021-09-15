---
title: ROTFlags
description: Controla el registro de un servidor COM en la tabla de objetos en ejecución (ROT).
ms.assetid: a27c04e5-b1d3-4cb5-9b2c-9ae45663cf56
keywords:
- COM valor del Registro ROTFlags
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d52bc0c07ee6c86015ad1b997f2f21e33dda9a1d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465967"
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

Se trata de **un valor \_ REG DWORD.**



| Valor de marca | Constante                        |
|------------|---------------------------------|
| 0x1        | **ROTREGFLAGS \_ ALLOWANYCLIENT** |



 

### <a name="rotregflags_allowanyclient-description"></a>Descripción de ROTREGFLAGS \_ ALLOWANYCLIENT

Si un servidor COM desea registrarse en rot y permitir que cualquier cliente acceda al registro, debe usar la marca **ROTFLAGS \_ ALLOWANYCLIENT.** Un servidor COM "Activar como activador" no puede especificar **ROTFLAGS \_ ALLOWANYCLIENT** porque el administrador de control de servicios DCOM (DCOMSCM) aplica una comprobación de suplantación de seguridad en esta marca. Por lo tanto, en Windows Vista y versiones posteriores, COM agrega compatibilidad con la entrada del Registro **ROTFlags** que permite al servidor estipular que sus registros ROT estén disponibles para cualquier cliente.

La entrada debe existir en el **subárbol HKEY \_ LOCAL \_ MACHINE.** Esta entrada proporciona un servidor "Activar como activador" con la misma funcionalidad que **ROTFLAGS \_ ALLOWANYCLIENT** proporciona para un servidor RunAs.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Clave appID](appid-key.md)
</dt> <dt>

[Registro de servidores COM](registering-com-servers.md)
</dt> <dt>

[Seguridad en COM](security-in-com.md)
</dt> </dl>

 

 




