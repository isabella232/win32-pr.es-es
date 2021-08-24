---
description: El método OpenDatabase del objeto Installer abre una base de datos existente o crea una nueva, devolviendo un objeto Database. Genera un error si el objeto Database no se puede crear ni abrir correctamente.
ms.assetid: a77b3954-db27-41a0-8f8b-2654766bde6a
title: Installer.OpenDatabase (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenDatabase
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: aab1e66dd4208817f854db88c57db5b6269a7a0b912242da649dffcf24cabab3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821375"
---
# <a name="installeropendatabase-method"></a>Installer.OpenDatabase (método)

El **método OpenDatabase** del objeto [**Installer**](installer-object.md) abre una base de datos existente o crea una nueva, devolviendo un [**objeto Database.**](database-object.md) Genera un error si el objeto **Database** no se puede crear ni abrir correctamente.

## <a name="syntax"></a>Sintaxis


```JScript
Installer.OpenDatabase(
  name,
  openMode
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*name* 
</dt> <dd>

Cadena necesaria que contiene el nombre de ruta de acceso de la base de datos. Si se proporciona una cadena vacía, se crea una base de datos temporal que no se conserva.

</dd> <dt>

*openMode* 
</dt> <dd>

Parámetro de la lista siguiente o una cadena que contiene el nombre de ruta de acceso del nuevo archivo de base de datos de salida en el que se va a escribir tras la confirmación.



| Parámetro                                                                                                                                                                                                                                                                                                                   | Significado                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiOpenDatabaseModeReadOnly"></span><span id="msiopendatabasemodereadonly"></span><span id="MSIOPENDATABASEMODEREADONLY"></span><dl> <dt>**msiOpenDatabaseModeReadOnly**</dt> <dt>0</dt> </dl>                 | Abre una base de datos de solo lectura, sin cambios persistentes.<br/>                                                                                                           |
| <span id="msiOpenDatabaseModeTransact"></span><span id="msiopendatabasemodetransact"></span><span id="MSIOPENDATABASEMODETRANSACT"></span><dl> <dt>**msiOpenDatabaseModeTransact**</dt> <dt>1</dt> </dl>                 | Abre una base de datos de lectura y escritura en modo de transacción.<br/>                                                                                                             |
| <span id="msiOpenDatabaseModeDirect"></span><span id="msiopendatabasemodedirect"></span><span id="MSIOPENDATABASEMODEDIRECT"></span><dl> <dt>**msiOpenDatabaseModeDirect**</dt> <dt>2</dt> </dl>                         | Abre una base de datos de lectura y escritura directa sin transacción.<br/>                                                                                                      |
| <span id="msiOpenDatabaseModeCreate"></span><span id="msiopendatabasemodecreate"></span><span id="MSIOPENDATABASEMODECREATE"></span><dl> <dt>**msiOpenDatabaseModeCreate**</dt> <dt>3</dt> </dl>                         | Crea una nueva base de datos, lectura y escritura en modo de transacción.<br/>                                                                                                            |
| <span id="msiOpenDatabaseModeCreateDirect"></span><span id="msiopendatabasemodecreatedirect"></span><span id="MSIOPENDATABASEMODECREATEDIRECT"></span><dl> <dt>**msiOpenDatabaseModeCreateDirect**</dt> <dt>4</dt> </dl> | Crea una nueva base de datos, lectura y escritura en modo directo.<br/>                                                                                                              |
| <span id="msiOpenDatabaseModeListScript"></span><span id="msiopendatabasemodelistscript"></span><span id="MSIOPENDATABASEMODELISTSCRIPT"></span><dl> <dt>**msiOpenDatabaseModeListScript**</dt> <dt>5</dt> </dl>         | Abre una base de datos para ver los archivos de script anunciados, como los archivos generados por [**el método CreateAdvertiseScript.**](installer-createadvertisescript.md)<br/> |
| <span id="msiOpenDatabaseModePatchFile"></span><span id="msiopendatabasemodepatchfile"></span><span id="MSIOPENDATABASEMODEPATCHFILE"></span><dl> <dt>**msiOpenDatabaseModePatchFile**</dt> <dt>32</dt> </dl>            | Agrega esta marca para indicar un archivo de revisión.<br/>                                                                                                                     |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Objeto [**Database**](database-object.md) que representa la base de datos existente o nueva del instalador que se abrió.

## <a name="remarks"></a>Comentarios

Cuando se abre una base de datos como salida de otra base de datos, el flujo de información de resumen de la base de datos de salida es realmente un reflejo de solo lectura de la base de datos original y, por tanto, no se puede cambiar. Además, no se conserva con la base de datos. Para crear o modificar la información de resumen de la base de datos de salida, debe cerrarse y volver a abrirse.

Para realizar y guardar los cambios en una base de datos, abra primero la base de datos en la transacción (msiOpenDatabaseModeTransact), cree (msiOpenDatabaseModeCreate o msiOpenDatabaseModeCreateDirect) o en modo directo (msiOpenDatabaseModeDirect). Después de realizar los cambios, llame siempre al [**método Commit**](database-commit.md) antes de cerrar el identificador de base de datos. El **método Commit** vacía todos los búferes.

Llame siempre al [**método Commit**](database-commit.md) en una base de datos que se haya abierto en modo directo (msiOpenDatabaseModeDirect o msiOpenDatabaseModeCreateDirect) antes de cerrar la base de datos. Si no lo hace, puede dañar la base de datos.

Dado que **el método OpenDatabase** inicia el acceso a la base de datos, no se puede usar con una instalación en ejecución.

Si se produce un error en el método , puede obtener información de error extendida mediante el [**método LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller se define como \_ 000C1090-0000-0000-C000-00000000046<br/>                                                                                                                                                                           |



 

 




