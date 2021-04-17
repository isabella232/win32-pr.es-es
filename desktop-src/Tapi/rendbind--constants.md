---
description: 'Las constantes RENDBIND son marcas usadas por el método ITDirectory:: BIND para indicar los tipos de autenticación proporcionados.'
ms.assetid: 27bcf36a-1826-4603-9821-22fcc5c1e186
title: Constantes de RENDBIND_ (Rend. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: badd2a48b2ae0632e317522533c664d4f74a6c77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690697"
---
# <a name="rendbind_-constants"></a>Constantes de RENDBIND \_

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

Las constantes RENDBIND son marcas usadas por el método [**ITDirectory:: Bind**](/windows/desktop/api/Rend/nf-rend-itdirectory-bind) para indicar los tipos de autenticación proporcionados.

<dl> <dt>

<span id="RENDBIND_AUTHENTICATE"></span><span id="rendbind_authenticate"></span>**autenticación de RENDBIND \_**
</dt> <dd> <dl> <dt>

 0x00000001
</dt> <dt>



Autenticar al usuario.


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



Usar contraseña predeterminada.


</dt> </dl> </dd> <dt>

<span id="RENDBIND_DEFAULTCREDENTIALS"></span><span id="rendbind_defaultcredentials"></span>**RENDBIND \_ DEFAULTCREDENTIALS**
</dt> <dd> <dl> <dt>

 0x0000000e
</dt> <dt>



Los tres elementos ORed anteriores juntos para mayor comodidad.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>Rend. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory)
</dt> <dt>

[**ITDirectory:: Bind**](/windows/desktop/api/Rend/nf-rend-itdirectory-bind)
</dt> </dl>

 

 




