---
description: La tabla SelfReg contiene información sobre los módulos que deben registrarse por sí mismos.
ms.assetid: 7fe5c96e-16a4-49c9-9a93-616608aa55b2
title: Tabla SelfReg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5895b1d23369a7c121547fed841731b5d3e76ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818550"
---
# <a name="selfreg-table"></a>Tabla SelfReg

La tabla SelfReg contiene información sobre los módulos que deben registrarse por sí mismos. El instalador llama a la función [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) durante la instalación del módulo; llama a [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) durante la desinstalación del módulo. El instalador no registra automáticamente los archivos EXE.

La tabla SelfReg tiene las columnas siguientes.



| Columna | Tipo                         | Clave | Nullable |
|--------|------------------------------|-----|----------|
| Archivo\_ | [Identificador](identifier.md) | Y   | N        |
| Costos   | [Entero](integer.md)       | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Filesystem\_
</dt> <dd>

Clave externa en la primera columna de la [tabla de archivos](file-table.md) que indica el módulo que se debe registrar.

</dd> <dt>

<span id="Cost"></span><span id="cost"></span><span id="COST"></span>Costará
</dt> <dd>

Costo de registrar el módulo en bytes. Debe ser un número no negativo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Se recomienda encarecidamente el uso del registro automático a los autores de paquetes de instalación. En su lugar, deben registrar los módulos mediante la creación de una o varias tablas proporcionadas por el instalador para este fin. Para obtener más información, consulte [grupo de tablas del registro](registry-tables-group.md). Muchas de las ventajas de tener un servicio de instalador central se pierden con el registro automático porque las rutinas de registro automático suelen ocultar la información de configuración crítica. Entre los motivos para evitar el registro propio se incluyen:

-   La reversión de una instalación con módulos autoregistrados no puede realizarse de forma segura con [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) porque no hay ninguna manera de indicar si otras características o aplicaciones usan las claves registradas automáticamente.
-   La capacidad de usar el anuncio se reduce si el registro de la clase o del servidor de extensiones se realiza en rutinas de registro automático.
-   El instalador controla automáticamente las claves HKCR en las tablas del registro para las instalaciones por usuario o por equipo. Actualmente, las rutinas de [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) no admiten la noción de una clave HKCR por usuario.
-   Si varios usuarios utilizan una aplicación autoregistrada en el mismo equipo, cada usuario debe instalar la aplicación la primera vez que la ejecuta. En caso contrario, el instalador no puede determinar fácilmente que existen las claves del registro HKCU apropiadas.
-   Se puede denegar el acceso a la red [**a los recursos**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) de red, como las bibliotecas de tipos, si un componente se especifica como Run-from-Source y aparece en la tabla SelfReg. Esto puede hacer que se produzca un error en la instalación del componente durante una instalación administrativa.
-   Los archivos dll de registro automático son más susceptibles a errores de codificación porque el nuevo código necesario para [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) es normalmente diferente para cada archivo dll. En su lugar, use las tablas del registro en la base de datos para aprovechar el código existente proporcionado por el instalador.
-   A veces, los archivos dll de registro automático pueden vincularse a archivos dll auxiliares que no estén presentes o que tengan una versión incorrecta. En cambio, el instalador puede registrar los archivos DLL mediante las tablas del registro sin depender del estado actual del sistema.

> [!Note]  
> No se puede especificar el orden en el que el instalador registra o anula el registro de los archivos dll de registro automático mediante las acciones [SelfRegModules](selfregmodules-action.md) y [SelfUnRegModules](selfunregmodules-action.md) . Vea [especificar el orden de registro automático](specifying-the-order-of-self-registration.md).

 

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 
