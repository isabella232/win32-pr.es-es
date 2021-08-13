---
description: La tabla SelfReg contiene información sobre los módulos que deben registrarse por sí solos.
ms.assetid: 7fe5c96e-16a4-49c9-9a93-616608aa55b2
title: Tabla SelfReg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d00b9f18755cf3284edfd1ba9476b12ba6343c816dbafe84ac3c3676f663f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625511"
---
# <a name="selfreg-table"></a>Tabla SelfReg

La tabla SelfReg contiene información sobre los módulos que deben registrarse por sí solos. El instalador llama a [**la función DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) durante la instalación del módulo; llama a [**DllUnregisterServer durante**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) la desinstalación del módulo. El instalador no registra archivos EXE de forma independiente.

La tabla SelfReg tiene las columnas siguientes.



| Columna | Tipo                         | Key | Nullable |
|--------|------------------------------|-----|----------|
| Archivo\_ | [Identificador](identifier.md) | Y   | N        |
| Coste   | [Entero](integer.md)       | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Archivo\_
</dt> <dd>

Clave externa en la primera columna de la [tabla Archivo](file-table.md) que indica el módulo que debe registrarse.

</dd> <dt>

<span id="Cost"></span><span id="cost"></span><span id="COST"></span>Costo
</dt> <dd>

Costo de registrar el módulo en bytes. Debe ser un número no negativo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Se recomienda encarecidamente a los autores de paquetes de instalación que no utilicen el registro propio. En su lugar, deben registrar módulos mediante la creación de una o varias tablas proporcionadas por el instalador para este propósito. Para obtener más información, vea [Grupo de tablas del Registro](registry-tables-group.md). Muchas de las ventajas de tener un servicio de instalador central se pierden con el registro automático porque las rutinas de registro automático tienden a ocultar información de configuración crítica. Entre los motivos para evitar el registro propio se incluyen:

-   La reversión de una instalación con módulos autoregistrados no se puede realizar de forma segura mediante [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) porque no hay ninguna manera de saber si otra característica o aplicación usa las claves autoregistradas.
-   La capacidad de usar anuncios se reduce si el registro del servidor de extensión o clase se realiza dentro de rutinas de registro propio.
-   El instalador controla automáticamente las claves HKCR en las tablas del Registro para las instalaciones por usuario o por máquina. Actualmente, las rutinas [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) no admiten la noción de clave HKCR por usuario.
-   Si varios usuarios usan una aplicación auto registrada en el mismo equipo, cada usuario debe instalar la aplicación la primera vez que la ejecute. De lo contrario, el instalador no puede determinar fácilmente que existen las claves del Registro HKCU adecuadas.
-   Se puede denegar el acceso a [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) a recursos de red como bibliotecas de tipos si un componente se especifica como run-from-source y se muestra en la tabla SelfReg. Esto puede hacer que la instalación del componente no se pueda realizar durante una instalación administrativa.
-   Los archivos DLL de registro propio son más susceptibles a errores de codificación porque el nuevo código necesario para [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) es normalmente diferente para cada archivo DLL. En su lugar, use las tablas del Registro de la base de datos para aprovechar el código existente proporcionado por el instalador.
-   A veces, los archivos DLL de registro propio pueden vincularse a archivos DLL auxiliares que no están presentes o que son una versión incorrecta. Por el contrario, el instalador puede registrar los archivos DLL mediante las tablas del Registro sin dependencia del estado actual del sistema.

> [!Note]  
> No se puede especificar el orden en el que el instalador registra o anula el registro de los archivos DLL autoregistros mediante las acciones [SelfRegModules](selfregmodules-action.md) y [SelfUnRegModules.](selfunregmodules-action.md) Vea [Especificar el orden de registro propio.](specifying-the-order-of-self-registration.md)

 

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 
