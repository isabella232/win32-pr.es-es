---
description: Cómo devolver registros de diario de cambios que cumplan los criterios especificados.
ms.assetid: 8946adb5-da47-4711-8800-86f323081c4c
title: Recorrer un búfer de registros de diario de cambios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9242d671cedfb5c9ef2b5fa836e29c455d09a9e1287b1ed035712f49c6c7d627
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830155"
---
# <a name="walking-a-buffer-of-change-journal-records"></a>Recorrer un búfer de registros de diario de cambios

Los códigos de control que devuelven registros de diario de cambio de número de secuencia de actualización (USN), [**FSCTL \_ READ \_ USN \_ JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) y [**FSCTL \_ ENUM \_ USN \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data), devuelven datos similares en el búfer de salida. Ambos devuelven un USN seguido de cero o más registros de diario de cambios, cada uno en una estructura [**USN \_ RECORD \_ V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) o [**USN \_ RECORD \_ V3.**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3)

El volumen de destino para las operaciones de USN debe ser ReFS o NTFS 3.0 o posterior. Para obtener la versión NTFS de un volumen, abra un símbolo del sistema con derechos de acceso de administrador y ejecute el siguiente comando:

**FSUtil.exe FSInfo NTFSInfo** *X::**

donde *X* es la letra de unidad del volumen.

En la lista siguiente se identifican las formas de obtener registros de diario de cambios:

-   Use [**FSCTL \_ ENUM \_ USN \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data) para obtener una lista (enumeración) de todos los registros de diario de cambios entre dos USN.
-   Use [**FSCTL \_ READ \_ USN \_ JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) para ser más selectivo, como seleccionar motivos específicos para los cambios o devolver cuando se cierra un archivo.

> [!Note]  
> Ambas operaciones devuelven solo el subconjunto de registros del diario de cambios que cumplen los criterios especificados.

 

El USN devuelto como primer elemento del búfer de salida es el USN del siguiente número de registro que se va a recuperar. Use este valor para seguir leyendo registros desde el límite final hacia delante.

El **miembro FileName** de [**USN RECORD \_ \_ V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) o [**USN RECORD \_ \_ V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) contiene el nombre del archivo al que se aplica el registro en cuestión. El nombre de archivo varía en longitud, por lo **que USN \_ RECORD \_ V2** y **USN RECORD \_ \_ V3** son estructuras de longitud variable. Su primer miembro, **RecordLength**, es la longitud de la estructura (incluido el nombre de archivo), en bytes.

Cuando trabaje con el miembro **FileName** de las estructuras [**USN \_ RECORD \_ V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) y [**USN \_ RECORD \_ V3,**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) no suponga que el nombre de archivo contiene un delimitador \\ "0" final. Para determinar la longitud del nombre de archivo, use el **miembro FileNameLength.**

En el ejemplo siguiente se [**llama a FSCTL \_ READ \_ USN \_ JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) y se recorre el búfer de los registros del diario de cambios que devuelve la operación.


```C++
#include <Windows.h>
#include <WinIoCtl.h>
#include <stdio.h>

#define BUF_LEN 4096

void main()
{
   HANDLE hVol;
   CHAR Buffer[BUF_LEN];

   USN_JOURNAL_DATA JournalData;
   READ_USN_JOURNAL_DATA ReadData = {0, 0xFFFFFFFF, FALSE, 0, 0};
   PUSN_RECORD UsnRecord;  

   DWORD dwBytes;
   DWORD dwRetBytes;
   int I;

   hVol = CreateFile( TEXT("\\\\.\\c:"), 
               GENERIC_READ | GENERIC_WRITE, 
               FILE_SHARE_READ | FILE_SHARE_WRITE,
               NULL,
               OPEN_EXISTING,
               0,
               NULL);

   if( hVol == INVALID_HANDLE_VALUE )
   {
      printf("CreateFile failed (%d)\n", GetLastError());
      return;
   }

   if( !DeviceIoControl( hVol, 
          FSCTL_QUERY_USN_JOURNAL, 
          NULL,
          0,
          &JournalData,
          sizeof(JournalData),
          &dwBytes,
          NULL) )
   {
      printf( "Query journal failed (%d)\n", GetLastError());
      return;
   }

   ReadData.UsnJournalID = JournalData.UsnJournalID;

   printf( "Journal ID: %I64x\n", JournalData.UsnJournalID );
   printf( "FirstUsn: %I64x\n\n", JournalData.FirstUsn );

   for(I=0; I<=10; I++)
   {
      memset( Buffer, 0, BUF_LEN );

      if( !DeviceIoControl( hVol, 
            FSCTL_READ_USN_JOURNAL, 
            &ReadData,
            sizeof(ReadData),
            &Buffer,
            BUF_LEN,
            &dwBytes,
            NULL) )
      {
         printf( "Read journal failed (%d)\n", GetLastError());
         return;
      }

      dwRetBytes = dwBytes - sizeof(USN);

      // Find the first record
      UsnRecord = (PUSN_RECORD)(((PUCHAR)Buffer) + sizeof(USN));  

      printf( "****************************************\n");

      // This loop could go on for a long time, given the current buffer size.
      while( dwRetBytes > 0 )
      {
         printf( "USN: %I64x\n", UsnRecord->Usn );
         printf("File name: %.*S\n", 
                  UsnRecord->FileNameLength/2, 
                  UsnRecord->FileName );
         printf( "Reason: %x\n", UsnRecord->Reason );
         printf( "\n" );

         dwRetBytes -= UsnRecord->RecordLength;

         // Find the next record
         UsnRecord = (PUSN_RECORD)(((PCHAR)UsnRecord) + 
                  UsnRecord->RecordLength); 
      }
      // Update starting USN for next call
      ReadData.StartUsn = *(USN *)&Buffer; 
   }

   CloseHandle(hVol);

}
```



El tamaño en bytes de cualquier registro especificado por una estructura [**USN \_ RECORD \_ V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) o [**USN \_ RECORD \_ V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) es como máximo donde `((MaxComponentLength - 1) * Width) + Size` *MaxComponentLength* es la longitud máxima en caracteres del nombre del archivo de registro. El ancho es el tamaño de un carácter ancho y *el tamaño* de la estructura.

Para obtener la longitud máxima, llame a la función [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) y examine el valor al que apunta el *parámetro lpMaximumComponentLength.* Resta uno de *MaxComponentLength* para tener en cuenta el hecho de que la definición de [**USN \_ RECORD**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) y [**USN \_ RECORD \_ V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) incluye un carácter del nombre de archivo.

En el lenguaje de programación C, el mayor tamaño de registro posible es el siguiente:

`(MaxComponentLength - 1) * sizeof(WCHAR) + sizeof(USN_RECORD)`

 

 
