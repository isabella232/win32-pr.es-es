---
title: Componentes de Windows instalados a petición
description: Componentes de Windows instalados a petición
ms.assetid: 14865DD7-167C-462C-B85A-BD07C929D7B8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09d2c3c3fee1cd12d7b12900e41dc006badcf53f
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "104078500"
---
# <a name="windows-components-installed-on-demand"></a>Componentes de Windows instalados a petición

## <a name="platform"></a>Plataforma

**Clientes-** Windows 8.1  







## <a name="description"></a>Descripción

Dos componentes de Windows se instalarán a petición en Windows 8.1: DirectPlay y NTVDM. Estos componentes se enumeran en componentes opcionales en el nodo "componentes heredados". Estos componentes se instalan localmente como parte del sistema operativo y se comprimen como componentes opcionales. Cuando una aplicación hace referencia o llama a uno de estos componentes (normalmente en el primer inicio de la aplicación), la instalación se desencadena automáticamente. Los usuarios recibirán una notificación de que el componente se instalará y deben confirmar la acción para poder continuar. La elevación es necesaria para que esto se realice correctamente si el usuario no es un administrador. Después de la instalación inicial, el usuario no necesita realizar ninguna otra acción para usar el componente de nuevo.

## <a name="manifestation"></a>Manifestación

Cuando una aplicación hace referencia o llama a un componente heredado en componentes opcionales (en el primer inicio), se suspenderá la aplicación y se abrirá el cuadro de diálogo de características a petición, que solicitará permiso al usuario para instalar el componente. Si los usuarios hacen clic en aceptar, también pueden ver una petición de elevación en la que deben escribir sus credenciales. A continuación, se instalará el componente y se reanudará la aplicación.

## <a name="mitigation"></a>Mitigación

Para evitar que se abra la interfaz de usuario de características a petición, puede preinstalar DirectPlay y NTVDM mediante DISM o la interfaz de usuario de componentes opcionales.

## <a name="solution"></a>Solución

Se recomienda encarecidamente evitar la referencia o la llamada a los componentes que se han enumerado como componentes opcionales heredados en Windows en versiones futuras de la aplicación. Los componentes opcionales heredados incluirán solo los componentes más antiguos y menos usados que podrían causar problemas de rendimiento y seguridad para los usuarios.

## <a name="tests"></a>Pruebas

No se necesitan alojamientos de prueba adicionales para la compatibilidad. Es importante tener en cuenta que este cuadro de diálogo aparecerá cuando se llame al componente opcional o se haga referencia a él, y esta instalación requiere elevación.

 

 




