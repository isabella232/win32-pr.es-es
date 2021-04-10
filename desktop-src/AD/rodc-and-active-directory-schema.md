---
title: Read-Only DCs y el esquema de Active Directory
description: Windows Server 2008 introduce un nuevo tipo de controlador de dominio, el controlador de dominio de solo lectura (RODC).
ms.assetid: 9d9082d2-6f7f-4ffa-b8c7-6414be764d0c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4284ffdda7ed2fbe481c201f7da69371209ce55
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104149701"
---
# <a name="read-only-dcs-and-the-active-directory-schema"></a>Read-Only DCs y el esquema de Active Directory

Windows Server 2008 introduce un nuevo tipo de controlador de dominio, el controlador de dominio de solo lectura (RODC). Esto proporciona un controlador de dominio para su uso en sucursales donde no se puede colocar un controlador de dominio completo. El objetivo es permitir que los usuarios de las sucursales inicien sesión y realicen tareas como el uso compartido de archivos e impresoras, incluso cuando no hay conectividad de red a sitios de concentrador.

RODC no cambia la forma en que se usa el esquema. Sin embargo, merece la pena mencionar que el esquema admite un conjunto de atributos parciales Read-Only (RO-PAS), también conocido como un conjunto de atributos filtrados de RODC, que es un conjunto de atributos especiales que no se replica en RODC por motivos de seguridad. RO-PAS se define en el esquema mediante el atributo [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) .

## <a name="rodc-filtered-attribute-set"></a>Conjunto de atributos filtrado de RODC

Algunas aplicaciones que usan [Active Directory Domain Services](active-directory-domain-services.md) como almacén de datos pueden tener datos similares a las credenciales (por ejemplo, contraseñas, credenciales o claves de cifrado) que no se deben almacenar en un controlador de dominio Read-Only en caso de que el RODC se robe o se ponga en peligro. Para este tipo de aplicación, puede Agregar el atributo al conjunto de atributos filtrados de RODC para impedir que se replique en RODC en el bosque, y marcar el atributo como confidencial, lo que elimina la capacidad de leer los datos de los miembros del grupo usuarios autenticados (incluidos los RODC).

## <a name="adding-attributes-to-the-rodc-filtered-attribute-set"></a>Agregar atributos al conjunto de atributos filtrados de RODC

El conjunto de atributos filtrados de RODC es un conjunto dinámico de atributos que no se replican en ningún RODC en el bosque. Puede configurar el conjunto de atributos filtrados de RODC en un maestro de esquema que ejecuta Windows Server 2008. Cuando los atributos no se pueden replicar en RODC, los datos no se pueden exponer innecesariamente si un RODC es robado o está en peligro.

No se pueden agregar atributos críticos del sistema al conjunto de atributos filtrados de RODC. Un atributo es crítico para el sistema si es necesario para AD DS, la autoridad de seguridad local (LSA), el administrador de cuentas de seguridad (SAM) y cualquiera de los proveedores de servicios de seguridad específicos de Microsoft, como el protocolo de autenticación Kerberos, para funcionar correctamente. En las versiones de Windows Server 2008 después de la versión beta 3, un atributo crítico para el sistema tiene un valor de atributo schemaFlagsEx de (valor de atributo schemaFlagsEx & 0x1 = **true**).

Para obtener instrucciones paso a paso sobre cómo agregar atributos al conjunto de atributos filtrados de RODC, vea [el Apéndice D de la guía paso a paso de los RODC]( /previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc772331(v=ws.10)).

## <a name="marking-attributes-as-confidential"></a>Marcar atributos como confidenciales

Además, se recomienda marcar como confidencial cualquier atributo que se configure como parte del conjunto de atributos filtrados de RODC. Para marcar un atributo como confidencial, tiene que quitar el permiso de lectura para el atributo del grupo usuarios autenticados. Marcar el atributo como confidencial proporciona una protección adicional frente a un RODC que se ve comprometido quitando los permisos necesarios para leer los datos similares a las credenciales. Para obtener más información acerca de cómo marcar atributos como confidenciales, consulte [el artículo 922836 en Microsoft Knowledge Base]( https://support.microsoft.com/kb/922836).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía paso a paso para controladores de dominio de solo lectura]( https://support.microsoft.com/kb/922836)
</dt> </dl>

 

 