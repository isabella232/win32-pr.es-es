---
title: Extensión del esquema
description: Cuando las clases o atributos existentes no se ajustan al tipo de datos que desea almacenar, puede que desee ampliar el esquema.
ms.assetid: 9a80ce29-8ff0-4324-8a2f-afd6c5d2272e
ms.tgt_platform: multiple
keywords:
- Schema AD , How to Extend
- Active Directory, Using, Schema
- Active Directory, Using, Schema, Extending the Schema, How to Extend
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bc30f7292c1c1077cc4e44a9f022a430af87bc3efe876a5c197b3fe370d3b95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188163"
---
# <a name="how-to-extend-the-schema"></a>Extensión del esquema

Cuando las clases o atributos existentes no se ajustan al tipo de datos que desea almacenar, puede que desee ampliar el esquema. Para obtener más información sobre cómo decidir cuándo extender el esquema, vea [Extender el esquema](extending-the-schema.md). Cuando haya decidido que se requiere la extensión de esquema, use el procedimiento siguiente para ampliar el esquema.

## <a name="verify-active-directory-functionality-before-you-apply-any-schema-extensions"></a>Compruebe Active Directory funcionalidad antes de aplicar las extensiones de esquema.

Compruebe Active Directory funcionalidad antes de actualizar el esquema para asegurarse de que la extensión de esquema continúa sin errores. Como mínimo, asegúrese de que todos los controladores de dominio del bosque estén en línea y realicen la replicación entrante.

**Para comprobar Active Directory funcionalidad antes de aplicar la extensión de esquema**

1.  Inicie sesión en una estación de trabajo administrativa que tenga Windows de soporte técnico Repadmin.exe instalado.
    > [!Note]  
    > Las herramientas de soporte técnico se encuentran en el medio de instalación del sistema operativo en la carpeta \\ Herramientas de soporte técnico.

     

2.  Abra un símbolo del sistema y, a continuación, cambie los directorios a la carpeta en la que Windows se instalan las herramientas de soporte técnico.
3.  En un símbolo del sistema, presione ENTER después de escribir:

    ``` syntax
    repadmin /replsum /bysrc /bydest /sort:delta
    ```

    Todos los controladores de dominio deben mostrar 0 en la columna Error y las diferencias más grandes (que indican el número de cambios realizados en la base de datos de Active Directory desde la última replicación correcta) deben ser menores o aproximadamente iguales a la frecuencia de replicación del vínculo de sitio que usa el controlador de dominio para la replicación. La frecuencia de replicación predeterminada es de 180 minutos.

    Para obtener más información sobre los pasos adicionales que puede realizar para comprobar la funcionalidad Active Directory antes de aplicar la extensión de esquema, consulte el artículo 325379 en [el Microsoft Knowledge Base](https://support.microsoft.com/kb/325379/en-us).

**Para extender el esquema**

1.  Determine el método de extensión. Una vez que haya diseñado cuidadosamente los cambios de esquema, el siguiente paso es decidir qué método usar para ampliar el esquema. Puede utilizar alguno de los siguientes métodos:
    -   Manualmente, mediante la importación de archivos. Consulte la documentación [Uso de la herramienta LDIFDE](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65)).
        > [!Note]  
        > No use LDIFDE para importar archivos Windows Sch \* .ldf. Estos archivos son necesarios para extender el esquema Active Directory con el fin de instalar controladores de dominio que ejecutan una versión más reciente de Windows Server que la versión que se ejecuta en el maestro de esquema actual. Cuando necesite extender el esquema para instalar un nuevo controlador de dominio, use Adprep.exe.

         

    -   Mediante programación, mediante un programa de instalación. Para obtener más información, vea [Extensión mediante programación.](programmatic-extension.md)
2.  Habilitar cambios de esquema. Para obtener más información, vea [Requisitos previos para instalar una extensión de esquema](prerequisites-for-installing-a-schema-extension.md) y Habilitar cambios de esquema en el maestro de [esquema](enabling-schema-changes-at-the-schema-master.md).
3.  Obtenga un identificador de objeto (OID) para los nuevos atributos o clases, como se describe en [Obtención de un identificador de objeto](obtaining-an-object-identifier.md).
4.  Cree nuevos atributos y clases.
5.  Use especificadores de visualización para integrar nuevos atributos y clases con la interfaz de usuario, si es necesario.
6.  Actualice la caché de esquemas como se describe en [Actualización de la caché de esquemas.](updating-the-schema-cache.md)
7.  Compruebe la extensión de esquema mediante LDP.exe.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Obtener un identificador de objeto](obtaining-an-object-identifier.md)
</dt> <dt>

[Nuevas herramientas de línea de comandos para Active Directory en Windows Server 2003](https://support.microsoft.com/kb/298882)
</dt> <dt>

[Uso de la herramienta LDIFDE](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65))
</dt> <dt>

[Extender el esquema Active Directory datos](/previous-versions/ms806972(v=msdn.10))
</dt> <dt>

[Restricciones en la extensión de esquema](restrictions-on-schema-extension.md)
</dt> </dl>

 

 