---
title: Cómo extender el esquema
description: Cuando las clases y los atributos existentes no se ajustan al tipo de datos que desea almacenar, puede que desee extender el esquema.
ms.assetid: 9a80ce29-8ff0-4324-8a2f-afd6c5d2272e
ms.tgt_platform: multiple
keywords:
- Esquema AD, cómo extender
- Active Directory, usar, esquema
- Active Directory, uso, esquema, extensión del esquema, cómo extender
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 437b23229182e6ec6f94b500feb764b4bbcf06e7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789520"
---
# <a name="how-to-extend-the-schema"></a>Cómo extender el esquema

Cuando las clases y los atributos existentes no se ajustan al tipo de datos que desea almacenar, puede que desee extender el esquema. Para obtener más información sobre cómo decidir cuándo ampliar el esquema, vea [extender el esquema](extending-the-schema.md). Una vez que haya decidido que se requiere la extensión de esquema, use el procedimiento siguiente para extender el esquema.

## <a name="verify-active-directory-functionality-before-you-apply-any-schema-extensions"></a>Comprobar la funcionalidad de Active Directory antes de aplicar las extensiones de esquema

Compruebe Active Directory funcionalidad antes de actualizar el esquema para asegurarse de que la extensión de esquema se prosigue sin errores. Como mínimo, asegúrese de que todos los controladores de dominio del bosque estén en línea y realice la replicación de entrada.

**Para comprobar la funcionalidad de Active Directory antes de aplicar la extensión de esquema**

1.  Inicie sesión en una estación de trabajo administrativa que tenga instalada la herramienta de soporte de Windows Repadmin.exe.
    > [!Note]  
    > Las herramientas de soporte se encuentran en los medios de instalación del sistema operativo en la \\ carpeta Herramientas de soporte.

     

2.  Abra un símbolo del sistema y, a continuación, cambie los directorios a la carpeta en la que están instaladas las herramientas de soporte de Windows.
3.  En un símbolo del sistema, presione ENTER después de escribir:

    ``` syntax
    repadmin /replsum /bysrc /bydest /sort:delta
    ```

    Todos los controladores de dominio deben mostrar 0 en la columna error, y las diferencias de mayor tamaño (que indican el número de cambios realizados en la base de datos de Active Directory desde la última replicación correcta) deben ser menores o iguales que la frecuencia de replicación del vínculo a sitios que utiliza el controlador de dominio para la replicación. La frecuencia de replicación predeterminada es de 180 minutos.

    Para obtener más información acerca de los pasos adicionales que puede realizar para comprobar la funcionalidad de Active Directory antes de aplicar la extensión de esquema, consulte [el artículo 325379 en Microsoft Knowledge Base](https://support.microsoft.com/kb/325379/en-us).

**Para extender el esquema**

1.  Determine el método de extensión. Una vez que haya diseñado cuidadosamente los cambios de esquema, el paso siguiente consiste en decidir qué método usar para extender el esquema. Puede utilizar alguno de los siguientes métodos:
    -   Manualmente, mediante el uso de archivos de importación. Consulte la documentación sobre el [uso de la herramienta LDIFDE](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65)).
        > [!Note]  
        > No use LDIFDE para importar archivos de Windows SCH \* . ldf. Estos archivos son necesarios para extender el esquema de Active Directory con el fin de instalar los controladores de dominio que ejecutan una versión más reciente de Windows Server que la versión que se está ejecutando en el maestro de esquema actual. Cuando necesite ampliar el esquema para instalar un nuevo controlador de dominio, use Adprep.exe.

         

    -   Mediante programación, con un programa de instalación. Para obtener más información, consulte [extensión de programación](programmatic-extension.md) .
2.  Habilite los cambios de esquema. Para obtener más información, vea [requisitos previos para instalar una extensión de esquema](prerequisites-for-installing-a-schema-extension.md) y [habilitar los cambios de esquema en el maestro de esquema](enabling-schema-changes-at-the-schema-master.md).
3.  Obtenga un identificador de objeto (OID) para los nuevos atributos o clases, como se describe en [obtener un identificador de objeto](obtaining-an-object-identifier.md).
4.  Cree nuevos atributos y clases.
5.  Use especificadores de presentación para integrar nuevos atributos y clases con la interfaz de usuario, si es necesario.
6.  Actualice la caché de esquema tal y como se describe en [actualizar la caché de esquema](updating-the-schema-cache.md).
7.  Compruebe la extensión de esquema mediante LDP.exe.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Obtener un identificador de objeto](obtaining-an-object-identifier.md)
</dt> <dt>

[Las nuevas herramientas de línea de comandos para Active Directory en Windows Server 2003](https://support.microsoft.com/kb/298882)
</dt> <dt>

[Usar la herramienta LDIFDE](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65))
</dt> <dt>

[Extender el esquema de Active Directory](/previous-versions/ms806972(v=msdn.10))
</dt> <dt>

[Restricciones en la extensión de esquema](restrictions-on-schema-extension.md)
</dt> </dl>

 

 