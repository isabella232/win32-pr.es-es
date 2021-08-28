---
description: Administrador de compatibilidad
ms.assetid: 72a77e83-ab18-438c-af11-fa6d55bf0180
title: Administrador de compatibilidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 504378dd4998118e0189a40d978b5649a0bc0215e88ff660d7cdafa6edf7602c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098545"
---
# <a name="compatibility-administrator"></a>Administrador de compatibilidad

## <a name="affected-platforms"></a>Plataformas afectadas

 **Clientes:** Windows 2000, Windows XP, Windows Vista, Windows 7  
**Servidores:** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2  


## <a name="description"></a>Descripción

La herramienta Administrador de compatibilidad, proporcionada por application Compatibility Toolkit (ACT), le permite resolver muchos de los posibles problemas de compatibilidad de aplicaciones antes de implementar una nueva versión de Windows en su organización, mediante:

-   Proporcionar correcciones de compatibilidad individuales, modos de compatibilidad y mensajes de AppHelp que puede usar para resolver problemas de compatibilidad específicos
-   Permite crear correcciones de compatibilidad personalizadas, modos de compatibilidad, mensajes de AppHelp y bases de datos de compatibilidad
-   Proporcionar una herramienta de consulta que le permita buscar correcciones instaladas en los equipos locales

## <a name="usage"></a>Uso

En el diagrama de flujo siguiente se muestran los pasos necesarios para usar el administrador de compatibilidad para crear las correcciones de compatibilidad, los modos de compatibilidad y los mensajes de AppHelp.



| &nbsp;    | &nbsp;  |  &nbsp;   | &nbsp;  | &nbsp; | &nbsp;  |  &nbsp;  |
|--------------------------------------------|----------|--------------------------------------------------------------------------------------------|----------|-----------------------------------------------------|----------|-----------------------------------------------------------------------------|
| Creación de una nueva base de datos de compatibilidad (.sdb) | **>** | Seleccione la aplicación y, a continuación, seleccione las correcciones de compatibilidad que se aplicarán a la aplicación. | **>** | Prueba de la aplicación con la nueva corrección de compatibilidad | **>** | Guarde la base de datos de compatibilidad y, a continuación, implemente la corrección en la empresa. |



 

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   [Aplicación de compatibilidad Toolkit descarga](/windows-hardware/get-started/adk-install)
-   [Uso del administrador de compatibilidad](/previous-versions/windows/it-pro/windows-7/cc749034(v=ws.10))
-   [Correcciones de compatibilidad conocidas, modos de compatibilidad y mensajes de AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))
-   [Pruebas y mitigación de problemas mediante las herramientas de desarrollo](/previous-versions/orphan-topics/ws.10/cc766461(v=ws.10))

 

 
