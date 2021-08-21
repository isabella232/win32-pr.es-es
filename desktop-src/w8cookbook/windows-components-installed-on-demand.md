---
title: Windows componentes instalados a petición
description: Windows componentes instalados a petición
ms.assetid: 14865DD7-167C-462C-B85A-BD07C929D7B8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 765768d2e16005ca0a465b53f076c64c6a30f31b8739113954ccc11959c8e0c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028803"
---
# <a name="windows-components-installed-on-demand"></a>Windows componentes instalados a petición

## <a name="platform"></a>Plataforma

**Clientes:** Windows 8.1  







## <a name="description"></a>Descripción

Dos Windows se instalarán a petición en Windows 8.1: DirectPlay y NTVDM. Estos componentes se enumeran en Componentes opcionales en el nodo "Componentes heredados". Estos componentes se instalan localmente como parte del sistema operativo y se comprimen como componentes opcionales. Cuando una aplicación hace referencia o llama a uno de estos componentes (normalmente en el primer inicio de la aplicación), la instalación se desencadena automáticamente. Se notificará a los usuarios que el componente se instalará y deben confirmar la acción para poder continuar. La elevación es necesaria para que esto se realiza correctamente si el usuario no es un administrador. Después de la instalación inicial, el usuario no necesita realizar ninguna otra acción para volver a usar el componente.

## <a name="manifestation"></a>Manifestación

Cuando una aplicación hace referencia o llama a un componente heredado en componentes opcionales (en el primer inicio), la aplicación se suspenderá y se abrirá el cuadro de diálogo Característica a petición, solicitando permiso de usuario para instalar el componente. Si los usuarios hacen clic en Aceptar, también pueden ver un aviso de elevación donde deben escribir sus credenciales. A continuación, se instalará el componente y se reanudará la aplicación.

## <a name="mitigation"></a>Mitigación

Para evitar que se abra la interfaz de usuario Características a petición, puede instalar previamente DirectPlay y NTVDM mediante DISM o la interfaz de usuario de componentes opcionales.

## <a name="solution"></a>Solución

Se recomienda encarecidamente evitar hacer referencia o llamar a componentes que se han enumerado como componentes opcionales heredados en Windows versiones futuras de la aplicación. Los componentes opcionales heredados solo incluirán componentes más antiguos y menos usados que podrían causar problemas de rendimiento y seguridad para los usuarios.

## <a name="tests"></a>Pruebas

No se necesita ninguna prueba adicional para la compatibilidad. Es importante tener en cuenta que este cuadro de diálogo aparecerá cuando se llame o se haga referencia al componente opcional, y esta instalación requiere elevación.

 

 




