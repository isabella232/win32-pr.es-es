---
description: Las constantes RENDBIND son marcas que usa el método ITDirectory::Bind para indicar los tipos de autenticación proporcionados.
ms.assetid: 27bcf36a-1826-4603-9821-22fcc5c1e186
title: RENDBIND_ constantes (Rend.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c618ed2cf5d9dda4c2ee14b331e3603f8021e9c5f4755e38ecfb5929b5f45c23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760868"
---
# <a name="rendbind_-constants"></a>Constantes RENDBIND \_

\[Los controles e interfaces de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

Las constantes RENDBIND son marcas que usa el método [**ITDirectory::Bind**](/windows/desktop/api/Rend/nf-rend-itdirectory-bind) para indicar los tipos de autenticación proporcionados.

<dl> <dt>

<span id="RENDBIND_AUTHENTICATE"></span><span id="rendbind_authenticate"></span>**AUTENTICACIÓN DE RENDBIND \_**
</dt> <dd> <dl> <dt>

 0x00000001
</dt> <dt>



Autenticación del usuario.


</dt> </dl> </dd> <dt>

<span id="RENDBIND_DEFAULTDOMAINNAME"></span><span id="rendbind_defaultdomainname"></span>**RENDBIND \_ DEFAULTDOMAINNAME**
</dt> <dd> <dl> <dt>

 0x00000002
</dt> <dt>



Use el nombre de dominio predeterminado.


</dt> </dl> </dd> <dt>

<span id="RENDBIND_DEFAULTUSERNAME"></span><span id="rendbind_defaultusername"></span>**RENDBIND \_ DEFAULTUSERNAME**
</dt> <dd> <dl> <dt>

 0x00000004
</dt> <dt>



Use el nombre de usuario predeterminado.


</dt> </dl> </dd> <dt>

<span id="RENDBIND_DEFAULTPASSWORD"></span><span id="rendbind_defaultpassword"></span>**RENDBIND \_ DEFAULTPASSWORD**
</dt> <dd> <dl> <dt>

 0x00000008
</dt> <dt>



Use la contraseña predeterminada.


</dt> </dl> </dd> <dt>

<span id="RENDBIND_DEFAULTCREDENTIALS"></span><span id="rendbind_defaultcredentials"></span>**CREDENCIALES PREDETERMINADAS DE RENDBIND \_**
</dt> <dd> <dl> <dt>

 0x0000000e
</dt> <dt>



Los tres anteriores ORed juntos para mayor comodidad.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Rend.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory)
</dt> <dt>

[**ITDirectory::Bind**](/windows/desktop/api/Rend/nf-rend-itdirectory-bind)
</dt> </dl>

 

 




